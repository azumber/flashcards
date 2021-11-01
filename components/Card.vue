<!-- Please remove this file from your project -->
<template>
  <div id="container" class="max-w-md p-9 rounded-3xl shadow-2xl">
    <h1>Flash Cards App</h1>
    <input v-model="inpQuestion" class="quest p-2" type="text" placeholder="write a question.."><br>
    <input v-model="inpAnswer" class="answer p-2" type="text" placeholder="write an answer.."><br>
    <button id="submit" class="text-white py-2 px-4 rounded" style="margin: 10px;" @click="addCard()">
      S U B M I T
    </button>
    <h1>My List</h1>
    <ul :v-for="item in questions">
      <li>{{ item }}</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Card',
  data () {
    return {
      questions: [],
      inpQuestion: '',
      inpAnswer: ''
    }
  },
  methods: {
    addCard () {

    }
  }
}
</script>

<style scoped>
*{
  margin: 10px;
  background: #353536;
}
#container{
  margin: 20px;
}
h1{
  color: white;
  text-align: center;
  font-size: 20px;
}
.quest, .answe, li {
  color: white;
  margin: 10px;
  width: 350px;
  border-radius: 10px;
}

button{
  width: 350px;
  background-color: #3D56B2;
}
button:active {
  color: white;
  background-color: #3D56B2;
  box-shadow: 1px 1px 3px 1px rgba(0.2, 0.2, 0.1, 0.2);
  transform: translateY(4px);
}
</style>
