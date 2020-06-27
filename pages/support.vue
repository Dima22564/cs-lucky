<template>
  <main class="cs-lucky-main">
    <div class="cs-lucky-container">
      <div class="cs-lucky-row">
        <div class="support-content">
          <div class="support__main">
            <div class="support__chats">
              <div class="supportChat">
                <div class="supportChat__img" />
                <div class="supportChat__text">
                  <p class="supportChat__name">
                    Support Center
                  </p>
                  <p class="supportChat__desc">
                    dfcew wfw effqwf qfwf wfdfv dfdsfv
                  </p>
                </div>
              </div>
              <div class="supportChat">
                <div class="supportChat__img" />
                <div class="supportChat__text">
                  <p class="supportChat__name">
                    Support Center
                  </p>
                  <p class="supportChat__desc">
                    dfcew wfw effqwf qfwf wfdfv dfdsfv
                  </p>
                </div>
              </div>
              <div class="supportChat">
                <div class="supportChat__img" />
                <div class="supportChat__text">
                  <p class="supportChat__name">
                    Support Center
                  </p>
                  <p class="supportChat__desc">
                    dfcew wfw effqwf qfwf wfdfv dfdsfv
                  </p>
                </div>
              </div>
              <div class="supportChat">
                <div class="supportChat__img" />
                <div class="supportChat__text">
                  <p class="supportChat__name">
                    Support Center
                  </p>
                  <p class="supportChat__desc">
                    dfcew wfw effqwf qfwf wfdfv dfdsfv
                  </p>
                </div>
              </div>
              <div class="supportChat supportChat_active">
                <div class="supportChat__img" />
                <div class="supportChat__text">
                  <p class="supportChat__name">
                    Support Center
                  </p>
                  <p class="supportChat__desc">
                    dfcew wfw effqwf qfwf wfdfv dfdsfv
                  </p>
                </div>
              </div>
            </div>

            <div class="support__messages">
              <div class="messages__top">
                <div class="supportChat">
                  <div class="supportChat__img" />
                  <div class="supportChat__text">
                    <p class="supportChat__name">
                      Support Center
                    </p>
                    <p class="supportChat__online">
                      <span class="circle" /> <span class="supportChat__desc">Online</span>
                    </p>
                  </div>
                </div>
              </div>

              <div class="messages__messages">
                <div class="supportMessage">
                  <img src="" alt="" class="supportMessage__img">
                  <div class="supportMessage__wrapper">
                    <p class="supportMessage__marks">
                      Angela
                    </p>
                    <p class="supportMessage__text">
                      Your payment might be delayed for 5-10 minutes. If money didn’t get transferred within an hour, please contact the support, write details of payment to Security Support
                    </p>
                    <p class="supportMessage__marks">
                      3:54 PM
                    </p>
                  </div>
                </div>
              </div>

              <form class="messages__bottom sendForm">
                <label for="file" class="sendForm__file">
                  <input id="file" class="sendForm__fileInput" type="file" name="file">
                </label>
                <textarea id="" name="" class="sendForm__text" placeholder="Your message" />
                <button class="sendForm__btn"></button>
              </form>
            </div>
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
export default {
  layout: 'default',
  components: {
    Chat,
    Footer
  }
}
</script>

<style lang="sass">
@import '../theme/_var'
.support
  &-content
    display: flex
    flex-direction: column
    justify-content: space-between
    width: 100%
    padding-right: 24px
  &__main
    display: flex
  &__chats
    width: 243px
    margin-right: 24px
    flex-shrink: 0
    overflow-y: auto
    height: calc(100vh - 96px - 24px - 58px - 16px)
  &__messages
    width: 100%
    border-radius: 24px
    background-image: linear-gradient(129deg, #2d2f33 1%, #272a2e 52%, #222529)
    box-shadow: $dark-shadow
.supportChat
  display: flex
  align-items: center
  padding: 16px
  cursor: pointer
  margin-bottom: 8px
  &_active
    box-shadow: inset 8px 8px 40px 0 rgba(9, 14, 20, 0.4), inset -4px -4px 8px 0 rgba(224, 224, 255, 0.04), inset 0 1px 1px 0 rgba(9, 14, 20, 0.4)
    background-image: linear-gradient(to bottom, #090e14, #222529 60%, #2d2f33)
    border-radius: 48px 12px 12px 48px
  &__online
    display: flex
    align-items: center
    .circle
      width: 6px
      height: 6px
      border-radius: 50%
      background: #00ffaa
      flex-shrink: 0
      margin-right: 4px
  &__img
    width: 48px
    height: 48px
    border-radius: 50%
    flex-shrink: 0
    box-shadow: 8px 8px 24px 0 rgba(9, 14, 20, 0.4), -4px -4px 8px 0 rgba(224, 224, 255, 0.04), 0 1px 1px 0 rgba(9, 14, 20, 0.4), inset 0 -2px 1px 0 rgba(9, 14, 20, 0.8)
    background-image: linear-gradient(to bottom, #383a3d, #2d2f33)
    display: flex
    align-items: center
    justify-content: center
    margin-right: 16px
  &__name
    font-size: 16px
    color: $white
    font-weight: 500
  &__text
    display: flex
    flex-direction: column
  &__desc
    color: rgba(224, 224, 255, 0.6)
    @extend %font-13-16
    font-weight: 500
    max-width: 128px
    overflow: hidden
    text-overflow: ellipsis
    white-space: nowrap
.messages
  &__top
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 12px
    padding: 8px
  &__messages
    overflow-y: auto
    height: calc(100% - 96px - 20px - 48px - 24px - 20px)
    padding: 0 24px
  &__bottom
    display: flex
    align-items: center
    justify-content: space-between
    padding: 20px 24px 24px 24px
.supportMessage
  display: flex
  align-items: flex-start
  margin-bottom: 24px
  &__img
    width: 36px
    height: 36px
    border-radius: 12px
    flex-shrink: 0
    margin: 20px 16px 0 0
  &__text
    padding: 8px 12px
    background-color: rgba(224, 224, 255, 0.02)
    border-radius: 7px 24px 24px 24px
    font-weight: 500
    color: $white
    max-width: 490px
    margin: 4px 0
  &__marks
    margin-left: 12px
    font-size: 10px
    line-height: 16px
    color: rgba(224, 224, 255, 0.4)
    font-weight: 500

.sendForm
  display: flex
  align-items: center
  justify-content: space-between
  &__fileInput
    display: none
  &__file
    width: 48px
    height: 48px
    border-radius: 50%
    background-color: rgba(224, 224, 255, 0.02)
    cursor: pointer
    flex-shrink: 0
  &__text
    width: 100%
    padding: 12px 16px
    border-radius: 12px
    background: rgba(224, 224, 255, 0.02)
    color: $white
    max-height: 96px
    height: 48px
    font-size: 16px
    line-height: 24px
    margin: 0 16px
    border: none
    resize: none
    &::placeholder
      color: rgba(224, 224, 255, 0.6)
  &__btn
    @extend %btn-refresh
    width: 48px
    height: 48px
    border-radius: 50%
    background: $main-gradient
    box-shadow: $main-shadow
    flex-shrink: 0
</style>
