<template>
  <form action="">
            <div class="form-group">
                <input type="text" placeholder="First Name" v-model="firstName">
            </div>
            <div class="form-group">
                <input type="text" placeholder="Last Name" v-model="lastName">
            </div>
            <div class="form-group">
                <input type="text" placeholder="Comment" v-model="comment">
            </div>
            <div class="form-group">
                <button @click="addFirends">ADD FRIEND</button>
            </div>
  </form>

  <FriendCard
  :friends="friends"
  />

</template>

<script>
import FriendCard from './FriendCard.vue';
export default {
    data(){
        return{
            friends:[],
            firstName:"",
            lastName:"",
            comment:"",
        }
    },
    components:{
        FriendCard
    },
   
    methods:{
        addFirends(e){
            e.preventDefault();
            let friendObj = {};
            friendObj.firstName=this.firstName.toUpperCase();
            friendObj.lastName=this.lastName.toUpperCase();
            friendObj.comment=this.comment;

            if(this.firstName !=="" && this.lastName !=="" && this.comment !==""){
                this.friends.push(friendObj);
            }
            console.log(this.friends);
        }
    }

}
</script>
<style>
   form{
    margin:auto;
    margin-top:20px;
    padding: 20px;
    border-radius: 10px;
    width: 70%;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
   }
   
    .form-group{
        margin-top: 7px;
    }
    input{
        padding: 8px;
        width: 96.6%;
    }
    button{
        color:white;
        background:rgb(6, 6, 186);
        border: none;
        width: 100%;
        padding: 10px;
        font-size: 15px;
    }

</style>