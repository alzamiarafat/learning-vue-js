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


<!--form handling-->
<!--    <h2>{{ formValues }}</h2>-->

<!--    <input type="number" v-model="formValues.text" placeholder="Click Here">-->
<!--    <p>Input Here: {{ formValues.text+10 }}</p>-->

<!--    <label>single selection</label>-->
<!--    <select v-model="formValues.singleValue">-->
<!--      <option value="red">red</option>-->
<!--      <option value="blue">blue</option>-->
<!--      <option value="green">green</option>-->
<!--    </select>-->
<!--    <h5>value {{ formValues.singleValue }}</h5>-->


<!--    <label>single selection</label>-->
<!--    <select v-model="formValues.multiValue" multiple>-->
<!--      <option value="red">red</option>-->
<!--      <option value="blue">blue</option>-->
<!--      <option value="green">green</option>-->
<!--    </select>-->
<!--    <h5>value {{ formValues.multiValue }}</h5>-->

<!--    <input type="checkbox" v-model="formValues.checked" id="work">-->
<!--    <label for="work">work form home?</label><br>-->

<!--    <input type="checkbox" v-model="formValues.multipleCheck" value="html" id="html">-->
<!--    <label for="html">HTML</label>-->
<!--    <input type="checkbox" v-model="formValues.multipleCheck" value="css" id="css">-->
<!--    <label for="css">CSS</label>-->
<!--    <input type="checkbox" v-model="formValues.multipleCheck" value="jquery" id="jquery">-->
<!--    <label for="jquery">JQUERY</label>-->

<!--    <button @click="submit()">submit</button>-->

    <h2>Full Name: {{ firstName }} {{ lastName }}</h2>
    <h3>Computed Full Name: {{ fullName }}</h3>
    <button @click="changeFullName('Hasib Arafat')">changeFullName</button>

    <P>Total: {{ items.reduce((total,crnt) => ( total += crnt.price ), 0) }}</P>
    <button @click="items.push({id: 4, name: 'headphone', price: 50})">Add item</button>
    <P>Computed Total: {{ total }}</P>



  </div>
</template>

<script>

/*import methods from "methods";*/

export default {
  name: 'App',
  data() {
    return {
      firstName: "AL Zami",
      lastName: "Arafat",
      items: [
          {
            id: 1,
            name: "mobile",
            price: 1000,
          },
        {
            id: 2,
            name: "tv",
            price: 500,
          },
        {
            id: 1,
            name: "laptop",
            price: 450,
          }
      ]
    }
      // form control
      // formValues: {
      //   text: '',
      //   name: 'john',
      //   baseMultiply: 5,
      //   baseValue: 10,
      //   counter: 0,
      //   singleValue: '',
      //   multiValue: [],
      //   checked:false,
      //   multipleCheck: []


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
    },
    submit(){
      console.log(this.formValues)
    },
    changeFullName(value){
      this.fullName = value
    }
  },
  computed: {
    fullName: {
      get(){
        return `${this.firstName} ${this.lastName}`
      },
      set(value){
        const name = value.split(' ')
        this.firstName = name[0]
        this.lastName = name[1]

      }
    },
    total () {
      return this.items.reduce((total, crrnt) => (total += crrnt.price),0)
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
