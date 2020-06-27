<template>
  <main class="cs-lucky-main">
    <div class="cs-lucky-container">
      <div class="cs-lucky-row">
        <div class="faqs-content">
          <div class="faqs__wrapper">
            <div class="faqs">
              <Faq class="faqs__faq" title="Chat rules" text="It is not allowed, if you use more than 1 account at the same time . One of the reasons is about using promo codes and stealing them from other people. For the use of multiple accounts, some measures may be applied: Promo codes bans, Deleting items, Withdrawal bans" />
              <Faq class="faqs__faq" title="Chat rules" text="It is not allowed, if you use more than 1 account at the same time . One of the reasons is about using promo codes and stealing them from other people. For the use of multiple accounts, some measures may be applied: Promo codes bans, Deleting items, Withdrawal bans" />
              <Faq class="faqs__faq" title="Chat rules" text="It is not allowed, if you use more than 1 account at the same time . One of the reasons is about using promo codes and stealing them from other people. For the use of multiple accounts, some measures may be applied: Promo codes bans, Deleting items, Withdrawal bans" />
              <Faq class="faqs__faq" title="Chat rules" text="It is not allowed, if you use more than 1 account at the same time . One of the reasons is about using promo codes and stealing them from other people. For the use of multiple accounts, some measures may be applied: Promo codes bans, Deleting items, Withdrawal bans" />
            </div>
            <div class="faqs__bg" />
          </div>
          <Footer />
        </div>
        <Chat />
      </div>
    </div>
  </main>
</template>

<script>
import Chat from '../components/Chat'
import Footer from '../components/Footer'
import Faq from '../components/Faq'
export default {
  layout: 'default',
  components: {
    Chat,
    Footer,
    Faq
  }
}
</script>

<style lang="sass">
.faqs
  overflow-y: auto
  height: calc(100vh - 56px - 16px - 98px - 24px)
  margin: -20px -24px 0 -20px
  padding: 20px 24px 0 20px
  &-content
    width: 100%
    padding-right: 24px
    display: flex
    flex-direction: column
    justify-content: space-between
  &__faq
    margin-bottom: 24px
  &__wrapper
    position: relative
  &__bg
    background-image: linear-gradient(to bottom, rgba(33, 36, 41, 0), #212429)
    position: absolute
    bottom: 0
    left: 0
    width: 100%
    height: 128px
</style>
