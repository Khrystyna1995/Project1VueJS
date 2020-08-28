<template>
  <div>
   <div class="add">
   <input id="inp" type="text" placeholder="Add to do" v-model="toDoNew">
   <button class="btn" @click="addItem" v-if="toDoList.length <= 10" >+</button>
   </div>
  
  <div class="remove">
 <ul>
        <li class="item" v-for="(list, index) in toDoList" :key="index">
          <span>{{list}}</span>
          <button class="btn1" @click="removeItem(index)">-</button>
        </li>
  </ul>
  </div>
 
    
  </div>
</template>

<script>
export default {
  name: 'App',
  data: () => {
    return{
      toDoList : ['Read the book', 'Go to work'],
      toDoNew: ''
      
    }
  },
methods: { 
    addItem(){
      this.toDoList.push(this.toDoNew)
      this.toDoNew = ''
      },

    removeItem(index){
      this.toDoList.splice(index, 1)
   }  
  }
} 
</script>

<style> 

.add, .item {
display: flex;
justify-content: space-around;
}

#inp{
  
    padding: 10px;
    font-size: 30px;
    border: 10px solid rgba(255, 255, 255, 0.5);
    -moz-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -webkit-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.5);
    -moz-appearance: none;
    -webkit-appearance: none;
    outline: none;
    color: #333;
    width: 50%; 
    
   
} 

.btn {
    padding: 10px;
    font-size: 30px;
    border: 10px solid rgba(255, 255, 255, 0.5);
    -moz-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -webkit-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.5);
    -moz-appearance: none;
    -webkit-appearance: none;
    outline: none;
    color: #333;
    width: 10%;
   
}


.item{
  position: relative;
    padding: 10px;
    font-size: 55px;
    border: 10px solid rgba(255, 255, 255, 0.5);
    -moz-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -webkit-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.5);
    -moz-appearance: none;
    -webkit-appearance: none;
    outline: none;
    color: #333;
     
}

.btn1 {
    position: absolute ;
    right: 125px;
    font-size: 30px;
    border: 10px solid rgba(255, 255, 255, 0.5);
    -moz-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -webkit-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.25) inset, 0 2px 10px rgba(0, 0, 0, 0.25);
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.5);
    -moz-appearance: none;
    -webkit-appearance: none;
    outline: none;
    color: #333;
    width: 10%;
   
}
</style>