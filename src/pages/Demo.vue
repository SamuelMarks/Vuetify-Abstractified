<template>
  <div>


    <Navbar title="Demo"><v-btn to="/" flat>Working</v-btn></Navbar>
    <v-flex ma-5 pa-5>
      <ExpansionPanel popout :items="panelData"></ExpansionPanel>
      <Card title="Demo" subtitle="Card">Content goes here</Card>
      <Table>Example Table</Table>
    </v-flex>

    <v-flex mb-5 class="text-md-center">
      <v-btn dark color="green" @click="visible = true">Show Snackbar</v-btn>
    </v-flex>

    <Snackbar :visible="visible" @closed="visible = false">Wow tasty!</Snackbar>

    <!-- <Card color="secondary" dark title="Code"><code>{{ msg }}</code></Card> -->


    <Footer class="bottom" tabColor="primary" copyright="Mark Sonnenschein" :links="links"></Footer>


  </div>
</template>


<style scoped>
  code {
    width: 500px;
  }
  .container{
    width: 90%;
    margin-top: 40px;
    margin-bottom: 40px;
  }
  .bottom {
    /* min-top: 100vh; */ /* ...NOTE: or something like this for footer */
  }
</style>

<script>
import * as components from '@/components'
export default {
  components,

  data: () => ({
    msg: `<Navbar title="Demo"><v-btn to="/" flat>Working</v-btn></Navbar>
    <v-flex ma-5 pa-5>
      <ExpansionPanel popout></ExpansionPanel>
      <Card title="Demo" subtitle="Card">Content goes here</Card>
      <Table>Example Table</Table>
    </v-flex>

    <v-flex mb-5 class="text-md-center">
      <v-btn dark color="green" @click="visible = true">Show Snackbar</v-btn>
    </v-flex>

    <Snackbar :visible="visible" @closed="visible = false">Wow tasty!</Snackbar>

    <Card color="accent" dark title="Code"><code>{{ msg }}</code></Card>


    <Footer class="bottom" tabColor="primary" copyright="Mark Sonnenschein" :links="links"></Footer>`,
    headers: [
      {
        text: 'Dessert (100g serving)',
        align: 'left',
        value: 'name'
      },
      { text: 'Calories', align: 'center', value: 'calories' },
      { text: 'Fat (g)', align: 'center', value: 'fat' },
      { text: 'Carbs (g)', align: 'center', value: 'carbs' },
      { text: 'Protein (g)', align: 'center', value: 'protein' },
      { text: 'Iron (%)', align: 'center', value: 'iron' }
    ],
    desserts: [
      {
        value: false,
        name: 'Frozen Yogurt',
        calories: 159,
        fat: 6.0,
        carbs: 24,
        protein: 4.0,
        iron: '1%'
      },
      {
        value: false,
        name: 'Ice cream sandwich',
        calories: 237,
        fat: 9.0,
        carbs: 37,
        protein: 4.3,
        iron: '1%'
      },
      {
        value: false,
        name: 'Eclair',
        calories: 262,
        fat: 16.0,
        carbs: 23,
        protein: 6.0,
        iron: '7%'
      },
      {
        value: false,
        name: 'Cupcake',
        calories: 305,
        fat: 3.7,
        carbs: 67,
        protein: 4.3,
        iron: '8%'
      },
      {
        value: false,
        name: 'Gingerbread',
        calories: 356,
        fat: 16.0,
        carbs: 49,
        protein: 3.9,
        iron: '16%'
      },
      {
        value: false,
        name: 'Jelly bean',
        calories: 375,
        fat: 0.0,
        carbs: 94,
        protein: 0.0,
        iron: '0%'
      },
      {
        value: false,
        name: 'Lollipop',
        calories: 392,
        fat: 0.2,
        carbs: 98,
        protein: 0,
        iron: '2%'
      },
      {
        value: false,
        name: 'Honeycomb',
        calories: 408,
        fat: 3.2,
        carbs: 87,
        protein: 6.5,
        iron: '45%'
      },
      {
        value: false,
        name: 'Donut',
        calories: 452,
        fat: 25.0,
        carbs: 51,
        protein: 4.9,
        iron: '22%'
      },
      {
        value: false,
        name: 'KitKat',
        calories: 518,
        fat: 26.0,
        carbs: 65,
        protein: 7,
        iron: '6%'
      }
    ],
    links: [
      'Home',
      'About Us',
      'Team',
      'Services',
      'Blog',
      'Contact Us'
    ],
    panelData: [
      { header: 'Home', content: 'Welcome' },
      { header: 'About Us', content: 'We are cool' },
      { header: 'Team', content: 'Hello there' },
      { header: 'Services', content: 'Awesome stuff' },
      { header: 'Contact Us', content: 'Please do' }
    ],
    visible: false
  })
}
</script>
