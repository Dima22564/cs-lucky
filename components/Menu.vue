<template>
  <div class="cs-lucky-container">
    <div class="cs-lucky-menu">
      <div class="cs-lucky-menu__left">
        <nuxt-link tag="div" to="/" class="cs-lucky-menu__logo">
          LOGO
        </nuxt-link>
        <div class="cs-lucky-menu__links">
          <nuxt-link exact to="/" tag="div" class="cs-lucky-menu__link" active-class="cs-lucky-menu__link_active">
            <HomeIcon class="icon icon-30" />
            <span>Home</span>
          </nuxt-link>
          <nuxt-link exact to="/faq" tag="div" class="cs-lucky-menu__link" active-class="cs-lucky-menu__link_active">
            <CommentIcon class="icon icon-30" />
            <span>FAQ</span>
          </nuxt-link>
          <nuxt-link to="/support" tag="div" class="cs-lucky-menu__link" active-class="cs-lucky-menu__link_active" exact>
            <ForumIcon class="icon icon-30" />
            <span>Support</span>
          </nuxt-link>
        </div>

        <div class="cs-lucky-menu__social">
          <a href="" class="cs-lucky-menu__social-link">
            <TelegramIcon />
          </a>
          <a href="" class="cs-lucky-menu__social-link">
            <VkIcon />
          </a>
          <div class="notifications">
            <div class="notifications__icon">
              <BellIcon class="icon-30" />
              <span class="notifications__num">20</span>
            </div>
          </div>
        </div>
      </div>

      <div class="cs-lucky-menu__right">
        <img src="/images/avatar.jpg" alt="" class="cs-lucky-menu__avatar">
        <div class="cs-lucky-menu__wrapper">
          <div class="cs-lucky-menu__text">
            <p class="cs-lucky-menu__name">
              vino_costa
            </p>
            <p class="cs-lucky-menu__balance">
              Balance: <span class="emp">$28,309</span>
            </p>
          </div>
        </div>
        <button class="cs-lucky-menu__add">
          <PlusIcon />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapMutations } from 'vuex'
import HomeIcon from 'vue-material-design-icons/Home.vue'
import CommentIcon from 'vue-material-design-icons/CommentQuestion.vue'
import ForumIcon from 'vue-material-design-icons/Forum.vue'
import TelegramIcon from 'vue-material-design-icons/Telegram.vue'
import VkIcon from 'vue-material-design-icons/Vk.vue'
import BellIcon from 'vue-material-design-icons/Bell.vue'
import PlusIcon from 'vue-material-design-icons/Plus.vue'
export default {
  computed: {
    ...mapGetters({
      getWindowSize: 'common/getWindowSize'
    })
  },
  mounted () {
    const that = this
    this.windowSize = window.innerWidth
    this.setWindowSize(window.innerWidth)
    window.addEventListener('resize', function () {
      const windowSize = window.innerWidth
      that.setWindowSize(windowSize)
    })
  },
  methods: {
    ...mapMutations({
      setWindowSize: 'common/setWindowSize'
    })
  },
  components: {
    HomeIcon,
    CommentIcon,
    ForumIcon,
    TelegramIcon,
    VkIcon,
    BellIcon,
    PlusIcon
  }
}
</script>

<style lang="sass">
@import '../theme/_var'
.cs-lucky-menu
  display: flex
  align-items: center
  border-bottom: 2px solid rgba(224, 224, 255, 0.06)
  margin: 0 0 0 -20px
  padding: 0 0 0 20px
  &__left
    padding-top: 34px
    display: flex
    align-items: flex-start
    width: 100%
  &__right
    max-width: 352px
    width: 100%
    background: #272a2e
    display: flex
    align-items: center
    padding: 16px 24px 16px 16px
  &__avatar
    border-radius: 50%
    flex-shrink: 0
    margin-right: 24px
  &__logo
    margin-right: 48px
  &__links
    display: flex
    align-items: center
  &__link
    display: flex
    align-items: center
    color: $gray
    cursor: pointer
    font-size: 16px
    padding-bottom: 34px
    position: relative
    user-select: none
    &:not(:last-child)
      margin-right: 48px
    &_active
      color: $white
      &::after
        width: 100%
        content: ''
        background: $main-color
        position: absolute
        height: 2px
        bottom: 0
        left: 0
      .icon
        color: $main-color
    .icon
      margin-right: 15px
  &__social
    display: flex
    align-items: center
    margin-right: 24px
    margin-left: auto
    &-link
      color: $gray
      &:not(:last-child)
        margin-right: 48px
  &__wrapper
    display: flex
    align-items: center
    margin-right: 24px
  &__name
    font-size: 20px
    line-height: 28px
    letter-spacing: -0.4px
  &__balance
    color: $gray
    .emp
      color: $white
  &__add
    @extend %btn-refresh
    display: flex
    align-items: center
    justify-content: center
    width: 48px
    height: 48px
    border-radius: 50%
    flex-shrink: 0
    margin-left: auto
    color: $white
    background-image: $main-gradient
    box-shadow: $main-shadow
.notifications
  &__icon
    cursor: pointer
    position: relative
  &__num
    color: $white
    @extend %font-13-16
    display: inline-block
    padding: 0 3px
    background: $main-color
    border-radius: 9px
    position: absolute
    top: -10px
    right: -10px
</style>
