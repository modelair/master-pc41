<template>
  <main>
    <section class="card">
      <FenixBird class="logo" width="3em" height="3em">
      </FenixBird>
      <div class="about">
        <div class="title row">
          <span>Мастер ПК 41</span>
          <FenixQr width="2em" height="2em" style="padding-left: 2em;">
          </FenixQr>
        </div>
        <div class="description">
          <br/>
          <span>
            Обслуживание компьютеров
            <br/>
            и ноутбуков на дому
          </span>
          <br/>
          <br/>
          <span>Качество выше</span>
          <br/>
          <span>Цены - ниже</span>
         <p></p>
          <div class="row buttons">
            <button class="phone-button" @click="clickTelephone">
              Позвонить
            </button>
            <TelegramLogo  @click="clickTelegram" width="2.5em" class="svg-button"
                          height="2.5em"></TelegramLogo>
            <WhatsAppLogo width="2.5em" height="2.5em" class="svg-button"
                          @click="clickWhatsApp"></WhatsAppLogo>
            <vk-logo class="svg-button" width="2.5em" height="2.5em" @click="clickVk">

            </vk-logo>
          </div>
        </div>

      </div>
    </section>

  </main>

</template>

<script setup>




import VkLogo from '@/components/VkLogo'
import WhatsAppLogo from '@/components/WhatsApp-Logo.vue'
import TelegramLogo from '@/components/TelegramLogo.vue'
import FenixBird from '@/components/Fenix-Bird'
import FenixQr from '@/components/Fenix-Qr'

const genTel = () => {
  return '+79246887970'
}
const clickTelephone = () => {
  document.location.href = 'tel://' + genTel()
}
const clickTelegram = () => {
  document.location.href = 'tg://resolve?domain=master_pc41'
}
const clickWhatsApp = () => {
  document.location.href = document.location.href = 'whatsapp://send?phone=' + genTel()
}
const clickVk = () => {
  document.location.href = document.location.href = 'https://vk.com/' + genTel()
}
</script>
<script>

// import RuleText from '@/components/RuleText.vue'

export default {
  name: 'HelloWorld',

  props: {
    msg: String
  }
}
</script>


<style scoped lang="scss">

a {
  margin: 0;
  padding: 0;
}
.logo {
  font-size: 6em;
}
.card {
  gap: 1ch;
  display: flex;
  flex-direction: row;
  /*align-items: center;*/
  justify-content: center;
}
@media screen and (max-width: 1024px)  {
  #app {
    font-size: 14px;
  }

}

@media screen and (max-width: 1024px)  {
  .card {
    flex-direction: column;
    align-content: center;
    text-align: center;
    justify-content: center;
    align-items: center;
  }


  .title {
    font-size: 10px;
  }
  .buttons {
    justify-content: center;
    }
  .description {

    padding-left: 0;
  }

}
.description {
  text-transform: uppercase;
  padding-left: 1em;
}
.row {
  display: flex;
  flex-direction: row;
  align-items: center;

}
.svg-button {
  cursor: pointer;
  &:hover {
    filter: brightness(1.1);
  }
}
.phone-button {
  &:hover {
    filter: brightness(1.1);
  }
  height: 1.9em;
  padding: .3em 1em .3em 1em;
  background: var(--primary-color);
  color: var(--background-color);
  border-radius: 1em;
  text-transform: uppercase;
  outline: 0;
  border: 0;
  cursor: pointer;
  font-size: inherit;
}

.about {
  align-items: flex-start;
  justify-content: flex-start;

  &--title {
    background: var(--primary-color);

    justify-content: space-between;

    color: var(--background-color);
    border-radius: 1em;
    padding: .2em .7em;
    text-transform: uppercase;

    font-size: 200%;
    margin: 0;
  }
}


h1 {

}

p {
  font-size: 150%;
}

main {
  flex-direction: column;
  height: 100%;
  min-height: 100vh;
  display: flex;
  gap: 1ch;
  align-items: center;
  justify-content: center;
}


</style>
