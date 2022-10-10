<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <main>
    <section class="container">
      <h1>Contato</h1>
    </section>
    <section class="contacts">
      <div class="contact" v-for="(contact, index) in contacts" :key="index">
        <div class="contact-title">{{ contact.title }}</div>
        <a :href="contact.link" target="_blank">{{ contact.label }}</a>
      </div>
    </section>
  </main>
</template>

<script>
  import api from '@/services/api';

  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Contato',
    data() {
      return {
        contacts: []
      }
    },
    mounted() {
      api.get('/contacts.json').then(response => {
        this.contacts = response.data;
      });
    }
  }
</script>

<style scoped>
  main {
    align-items: flex-start;
    margin-left: 20px;
  }

  .contacts {
    margin-bottom: 40px;
    color: var(--color-text-dark);
  }

  .contact-title {
    font-weight: 600;
    font-size: 18px;
  }

  .contact a {
    color: var(--color-text-dark);
  }

  .contact {
    margin-bottom: 20px;
  }
</style>
