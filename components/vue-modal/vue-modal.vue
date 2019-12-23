<template>
  <div class="modal-vue">
    <div
      v-if="isOpen"
      class="modal-vue-wrapper"
      :class="[animationParent,{'modal-vue-wrapper-show' : open}]"
    >
      <div
        :class="['modal-vue-overlay']"
        :style="{backgroundColor:bgOverlay}"
        @click="$emit('hide')"
      />
      <div
        :class="['modal-vue-panel',animationPanel,{'modal-vue-show':open}]"
        :style="{width:width,backgroundColor:bgPanel}"
      >
        <div
          v-if="showCloseButton"
          class="modal-vue---close-icon"
          @click="$emit('hide')"
        >
          <slot name="close-icon">
            <div class="modal-vue---close-icon--default">
              &times;
            </div>
          </slot>
        </div>
        <div class="modal-vue--content">
          <div class="modal-vue--content-panel">
            <slot />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { disableBodyScroll, enableBodyScroll } from 'body-scroll-lock'

const bodyScrollOptions = {
  reserveScrollBarGap: true
}

export default {
  props: {
    visible: {
      type: Boolean,
      required: false,
      default: false
    },
    resizeWidth: {
      type: Object,
      default () {
        return { 780: '100%' }
      }
    },
    animationPanel: {
      type: String,
      required: false,
      default: 'modal-fade'
    },
    bgOverlay: {
      type: String,
      required: false,
      default: 'rgba(0, 0, 0, 0.57)'
    },
    bgPanel: {
      type: String,
      required: false,
      default: '#fff'
    },
    animationParent: {
      type: String,
      required: false,
      default: 'modal-fade'
    },
    defaultWidth: {
      type: String,
      required: false,
      default: '80%'
    },
    closeScroll: {
      type: Boolean,
      required: false,
      default: true
    },
    showCloseButton: {
      type: Boolean,
      required: false,
      default: true
    },
    showBackButton: {
      type: Boolean,
      required: false,
      default: true
    }
  },
  data () {
    return {
      width: this.defaultWidth || '80%',
      open: false,
      isOpen: false,
      isShowCloseButton: true,
      backups: {
        body: {
          height: null,
          overflow: null,
          paddingRight: null
        }
      }
    }
  },
  watch: {
    visible (val) {
      if (val) {
        this.isOpen = true
        this.$nextTick(() => {
          const panel = this.$el.querySelector('.modal-vue-panel')
          const offset = (this.windowHeight - panel.clientHeight) / 2
          if (offset > 50) {
            panel.style.top = (offset - 50) + 'px'
          }
          this._lockBody()
        })
        setTimeout(() => (this.open = true), 30)
        if (this.closeScroll) {
          // this._lockBody()
        }
      } else {
        const panel = this.$el.querySelector('.modal-vue-panel')
        panel.style.top = '0px'
        if (this.closeScroll) {
          this._unlockBody()
        }
        this.open = false
        setTimeout(() => (this.isOpen = false), 300)
      }
    }
  },

  beforeDestroy () {
    window.removeEventListener('resize', this.getWindowWidth)
    window.removeEventListener('resize', this.getWindowHeight)
  },
  destroyed () {
    if (this.open) {
      if (this.closeScroll) {
        this._unlockBody()
      }
      this.open = false
      setTimeout(() => (this.isOpen = false), 300)
    }
  },
  mounted () {
    this.$nextTick(function () {
      window.addEventListener('resize', this.getWindowWidth)
      window.addEventListener('resize', this.getWindowHeight)
      this.getWindowWidth()
      this.getWindowHeight()
    })
  },
  methods: {
    // getScrollbarWidth () {
    //   const outer = document.createElement('div')
    //   outer.style.visibility = 'hidden'
    //   outer.style.width = '100px'
    //   outer.style.msOverflowStyle = 'scrollbar' // needed for WinJS apps
    //
    //   document.body.appendChild(outer)
    //
    //   const widthNoScroll = outer.offsetWidth
    //   // force scrollbars
    //   outer.style.overflow = 'scroll'
    //
    //   // add innerdiv
    //   const inner = document.createElement('div')
    //   inner.style.width = '100%'
    //   outer.appendChild(inner)
    //
    //   const widthWithScroll = inner.offsetWidth
    //
    //   // remove divs
    //   outer.parentNode.removeChild(outer)
    //
    //   return widthNoScroll - widthWithScroll
    // },
    getWindowHeight (event) {
      this.windowHeight = document.documentElement.clientHeight
    },
    getWindowWidth (event) {
      // if (this.open) {
      if (this.resizeWidth && Object.keys(this.resizeWidth).length > 0) {
        this.windowWidth = document.documentElement.clientWidth
        const filter = Object.keys(this.resizeWidth).find(
          f => f >= this.windowWidth
        )
        if (filter) {
          this.width = this.resizeWidth[filter]
        } else {
          this.width = this.defaultWidth
        }
      }
      // }
    },
    _lockBody () {
      this.$nextTick(() => {
        window.disableBodyScroll = disableBodyScroll
        disableBodyScroll(this.$el.querySelector('.modal-vue-panel'), bodyScrollOptions)
      })
      // this.backups.body.height = document.body.style.height
      // this.backups.body.overflow = document.body.style.overflow
      // document.body.style.paddingRight = this.getScrollbarWidth() + 'px'
      // document.body.style.height = '100%'
      // document.body.style.overflow = 'hidden'
    },
    _unlockBody () {
      enableBodyScroll(this.$el.querySelector('.modal-vue-panel'), bodyScrollOptions)
      // document.body.style.height = this.backups.body.height
      // document.body.style.overflow = this.backups.body.overflow
      // document.body.style.paddingRight = this.backups.body.paddingRight
    }
  }
}
</script>
<style lang="scss" src="./vue-modal.scss" />
