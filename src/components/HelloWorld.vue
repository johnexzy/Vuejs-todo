<template>
  <div class="hello">
    <div class="holder">
      <form @submit.prevent="addSkill">
        <input type="text" placeholder="Enter a skill you have..." v-model="skill">
        <!-- {{skill}} -->
        <input type="checkbox" id="checkbox" v-model="checked">
      </form>
      <ul>
        <li v-for="(data, index) in skills" :key="index">{{data.skill}}</li>
      </ul>
      <p v-bind:style="{color:'#3b5998'}">You have {{skills.length}} skills</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data (){
    return{
      checked: false,
      skill: '',
      skills: [{skill: "Vuejs Developer"},{skill: "Front-End Developer"}],
      
    }
  
  },
  methods:{
    addSkill() {
      this.skills.push({skill: this.skill})
      this.skill = '';
      console.log('the checkbox is '+this.checked)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.holder{
  background:#fff;
  padding-bottom: 1px
}
ul{
  margin: 0;
  padding: 0;
  list-style-type: none;
}
ul li{
  padding: 20px;
  font-size:1.3em;
  background-color: #e0edf4;
  border-left: 5px solid #3eb3f6;
  color:#3e5252;
  margin-bottom: 2px;
}
p{
  text-align: center;
  margin: 30px 0;
  color: gray;
}
.container{
  box-shadow: 0px 0px 40px lightgray;
}
input{
  width: calc(100% - 40px);
  border: 0;
  padding: 20px;
  font-size: 1.3em;
  background-color: #323333;
  color: #687f7f;
}
</style>
