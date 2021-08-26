<template>
  <div>
<!--    <p v-html="text"></p>-->
<!--    <h3>Hello {{ name }}</h3>-->
<!--    <p :id="textID">fdsihgf</p>-->
<!--    <button :disabled="isDisabled">Apply</button>-->
<!--    <p class="underLine">Under Line text</p>-->
<!--    <p class="underLine" :class="status">gjsfh</p>-->
<!--    <h3 :class="isPromoted && 'promoted'">dfghfh</h3>-->
<!--    <h2 :class="isSoldout ? 'sold-out' : 'new'">stock</h2>-->
<!--    <h2 :class="['promoted','new']">array</h2>-->
<!--    <h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">conditional array</h2>-->
<!--    <h2 :class="{promoted: isPromoted,new:isSoldout,'sold_out':isSoldout}">conditional object</h2>-->
<!--    <p :style="{color: highlightcolor,fontSize:headerSize+'px',padding: '15px'}">Inline style</p>-->
<!--    <p :style="headerStyle">Style Object style</p>-->
<!--    <h2 v-if="num === 0">The number is zero</h2>-->
<!--    <h2 v-else>The number is not zero</h2>-->


<!--    <h2 v-for="(name, index) in names" :key="name">{{ index+1}}=>{{ name }}</h2>
    <h2 v-for="(name, index) in fullName" :key="name">{{ index+1}}.{{ name.firstName }} {{ name.lastName }}</h2>
    <div v-for="(post, index) in posts" :key="post.post">
      <h2>{{ index+1 }}.{{ post.post }}</h2>
      <p v-for="comment in post.comments" :key="comment">{{ comment }}</p>
    </div>
    <h1>Conditional list view</h1>
    <template v-for="name in names" :key="name">
      <p v-if="name === 'Bruce' ">{{ name }}</p>
    </template>-->


<!--    <h2>Add Method {{ add(1,2,3) }}</h2>-->
<!--    <h2>Multiply Method {{ multiply(20) }}</h2>-->
<!--    <h2>Multiply Method {{ multiply(baseValue) }}</h2>-->
<!--    <h1>{{ name }}</h1>-->
<!--    <button v-on:click="name = 'superman'">Change</button>-->
<!--    <h1> {{ counter }}</h1>-->
<!--    <button @click="increment()">+</button>-->
<!--    <button v-on:click="decrement()">-</button>-->

    <input type="number" v-model="text" placeholder="Click Here">
    <p>Input Here: {{ text+10 }}</p>


  </div>
</template>

<script>

/*import methods from "methods";*/

export default {
  name: 'App',
  data() {
    return{
      text: '',
      name: 'john',
      baseMultiply: 5,
      baseValue: 10,
      counter: 0
      /*name:'Batman',
      text: '<b>fdsga</b>',
      textID: 'test_id',
      isDisabled: false,
      status: 'danger',
      isPromoted: true,
      isSoldout: true,
      highlightcolor: 'orange',
      headerSize:50,
      headerStyle: {
        color: 'blue',
        fontSize: '20px',
        padding: '15px'
      },
      num: 0,*/
      // names: ['Bruce', 'Clark', 'Diana'],
      // fullName: [
      //   {firstName: 'Bruce', lastName: 'Wayne'},
      //   {firstName: 'Clark', lastName: 'Wayne'},
      //   {firstName: 'Diana', lastName: 'Wayne'},
      // ],
      // posts: [
      //   { post: 'This is a first post',
      //     comments: ['this is a 1st comment for first post','this is a 2nd comment','this is a 3rd comment']
      //   },
      //   { post: 'This is a second post',
      //     comments: ['this is a 1st comment','this is a 2nd comment','this is a 3rd comment']
      //   },
      //   { post: 'This is a third post',
      //     comments: ['this is a 1st comment','this is a 2nd comment','this is a 3rd comment']
      //   }
      // ]
    }
  },
  methods: {
    add(a,b,c) {
      return a+b+c
    },
    multiply(num) {
      return num * this.baseMultiply
    },
    increment() {
      return this.counter += 1
    },
    decrement() {
      return this.counter -= 1
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underLine{
  text-decoration: underline;
}
.promoted{
  font-style: italic;
}
.new{
  color: #42b983;
}
.sold-out{
  color: red;
}
</style>
