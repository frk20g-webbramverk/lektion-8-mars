<template>
  <section>
    <input type="text" placeholder="Ditt förnamn" v-model="name.firstName" />
    <input type="text" placeholder="Ditt efternamn" v-model="name.lastName" />
    <button v-on:click="save">Spara</button>
    <button v-on:click="remove">Radera</button>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: {
        firstName: '',
        lastName: ''
      },
      names: []
    }
  },
  methods: {
    save: function() {
      const copyName = Object.assign({}, this.name);
      this.names.push(copyName);
      window.localStorage.setItem('name', JSON.stringify(this.names));
    },
    remove: function() {
      const names = JSON.parse(window.localStorage.getItem('name'));
      console.log(names);
      const newNames = names.filter((name) => { return name.firstName !== 'Christoffer' });
      console.log(newNames);
      window.localStorage.setItem('name', JSON.stringify(newNames));
      //Tar bort alla namn
      //window.localStorage.removeItem('name');
    }
  }
}
</script>

<style>

</style>