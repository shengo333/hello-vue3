<template>
  <div>
    <pre>{{JSON.stringify(formValues,null,2)}}</pre>
    <form @submit.prevent="submitForm">
      <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model.trim.lazy="formValues.name">
      </div>
      <div>
        <label for="profile">Profile Summary is here</label>
        <textarea id="profile" v-model="formValues.profileSummary"></textarea>
      </div>

      <div>
        <label for="country">country is here</label>
        <select id="country" v-model="formValues.country">
          <option value="">select a country</option>
          <option value="Germany">Germany</option>
          <option value="India">India</option>
          <option value="Georgia">Georgia</option>
          <option value="USA">Singapore</option>
        </select>
      </div>
      <div>
        <label for="job-location">Job Location</label>
        <select id="job-location" multiple v-model="formValues.jobLocation" >
          <option value="">select a country</option>
          <option value="Germany">Germany</option>
          <option value="India">India</option>
          <option value="Georgia">Georgia</option>
          <option value="USA">Singapore</option>
        </select>
      </div>
      <div>
          <label>skill set</label>
          <input type="checkbox" id="html" value="html" v-model="formValues.skillSet"/>
          <label for="html" >HTML</label>
          <input type="checkbox" id="css" value="css" v-model="formValues.skillSet"/>
          <label for="css">css</label>
          <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet"/>
          <label for="javascript">javascript</label>
      </div>
      <div>
          <label>experience</label>
          <input type="radio" id="1-5" value="1-5" v-model="formValues.experience"/>
          <label for="1-5" >1-5</label>
          <input type="radio" id="6-10" value="6-10" v-model="formValues.experience"/>
          <label for="6-10" >6-10</label>
          <input type="radio" id="10+" value="10+" v-model="formValues.experience"/>
          <label for="10+" >10+</label>

      </div>

      <div>
        
        <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
        <label for="remoteWork"> open to remote work</label>
      </div>
      <div>
        
        <label for="age"> Age </label>
        <input @keyup.enter="submitForm" type="number" id="age" v-model.number="formValues.age">
      </div>
      <!-- <div>
        <button>Submit</button>
      </div> -->

    </form>


  </div>
</template>

<script>

export default {
  name: "App",
  data() {
    return{
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobLocation: [],
        remoteWork: 'no',
        skillSet:[],
        experience: '',
        age: null
      }
    }
  },
  methods:{
    submitForm(){
      console.log('Form values name is this one and the rest if inputed data', this.formValues)
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

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
  
}

input label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'],
textarea,
select{
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.32857143;
  color: #555;
  background-color: #fff;
  background-image: none;
}

form{
  padding: 30px;
}

</style>
