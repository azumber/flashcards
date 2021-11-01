<template>
  <div id="container" class="max-w-md p-9 rounded-3xl shadow-2xl">
    <h1>Flash Cards App</h1>
    <input v-model="card.inpQuestion" class="quest p-2" type="text" placeholder="write a question.."><br>
    <input v-model="card.inpAnswer" class="answer p-2" type="text" placeholder="write an answer.."><br>
    <button id="submit" class="text-white py-2 px-4 rounded" style="margin: 10px;" @click="addCard">
      S U B M I T
    </button>
    <h1>My List</h1>
    <div class="text-white py-2 px-4 rounded">
      <h3 v-for="item in questions" :key="item.id" @click="toggleShow">
        {{ item.inpQuestion }}
        <p v-if="isShowing" :id="item.id">
          {{ item.inpAnswer }}
        </p>
      </h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  data () {
    return {
      isShowing: false,
      count: 1,
      questions: [],
      card: {
        inpQuestion: '',
        inpAnswer: ''
      }
    }
  },
  methods: {
    addCard () {
      if (this.card.inpQuestion != null && this.card.inpAnswer != null) {
        this.questions.push({ id: this.count, ...this.card })
      }
      this.count++
      this.card = {}
    },
    toggleShow () {
      this.isShowing = !this.isShowing
    }
  }
}
</script>

<style scoped>
*{
  margin: 10px;
  background: #082032;
}
#container{
  margin: 20px;
}
h1{
  color: white;
  font-size: 20px;
  text-align: center;
}

h3 {
  font-size: 20px;
  width: 300px;
  text-align: center;
  border-radius: 10px;
  background-color: #052842;
  box-shadow: 1px 1px 3px 1px rgba(0.2, 0.2, 0.1, 0.2);
}
p {
  background-color: #052842;
}

input:focus{
  outline: none;
}

.quest, .answer {
  margin: 10px;
  width: 350px;
  color: white;
  border-radius: 10px;
  text-decoration: none;
}

button{
  width: 350px;
  background-color: #3D56B2;
  box-shadow: 1px 1px 3px 1px rgba(0.2, 0.2, 0.1, 0.2);
}
button:active {
  color: white;
  background-color: #3D56B2;
  box-shadow: 1px 1px 3px 1px rgba(0.2, 0.2, 0.1, 0.2);
  transform: translateY(4px);
}
</style>
