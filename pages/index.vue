<template>
  <div>
    <h1 class="bg-red-600">dimple success project</h1>

    <header>
        <ul class="flex bg-red-600">
  <li class="mr-6">
    <!-- <a class="text-blue-500 hover:text-blue-800" NuxtLink to="/home">Home</a> -->
    <NuxtLink to="/home">home</NuxtLink>
  </li>
  <li class="mr-6">
    <a class="text-blue-500 hover:text-blue-800" NuxtLink to="/user">Users</a>
  </li>
  <li class="mr-6">
    <a class="text-blue-500 hover:text-blue-800" NuxtLink to="/user">Contact Us</a>
  </li>
  
</ul>
    </header>











<section class="ml-96 mt-11 mb-11">
    <div>
        <div class="block p-6 rounded-lg shadow-lg bg-white max-w-sm">
  <form onsubmit="event.preventDefault();onFormSubmit();" autocomplete="off">
    <div class="form-group mb-6">
      <label for="exampleInputEmail1" class="form-label inline-block mb-2 text-gray-700">Name</label>
      <input type="name" class="form-control
        block
        w-full
        px-3
        py-1.5
        text-base
        font-normal
        text-gray-700
        bg-white bg-clip-padding
        border border-solid border-gray-300
        rounded
        transition
        ease-in-out
        m-0
        focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" id="name"
        aria-describedby="emailHelp" v-model="user.name"  placeholder="Enter name">
      
    </div>

    




    
    <div class="form-group mb-6">
      <label for="exampleInputPassword1" class="form-label inline-block mb-2 text-gray-700">Email</label>
      <input type="user.Email" class="form-control block
        w-full
        px-3
        py-1.5
        text-base
        font-normal
        text-gray-700
        bg-white bg-clip-padding
        border border-solid border-gray-300
        rounded
        transition
        ease-in-out
        m-0
        focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" id="Email" v-model="user.email"
        placeholder="Email">
    </div>



    <div class="form-group mb-6">
      <label for="exampleInputPassword1" class="form-label inline-block mb-2 text-gray-700">Phone no</label>
      <input type="Phone no" class="form-control block
        w-full
        px-3
        py-1.5
        text-base
        font-normal
        text-gray-700
        bg-white bg-clip-padding
        border border-solid border-gray-300
        rounded
        transition
        ease-in-out
        m-0
        focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" id="Phone no" v-model="user.phone"
        placeholder="Phone no">
    </div>


    <div class="form-group mb-6">
      <label for="exampleInputPassword1" class="form-label inline-block mb-2 text-gray-700">State</label>
      <input type="State" class="form-control block
        w-full
        px-3
        py-1.5
        text-base
        font-normal
        text-gray-700
        bg-white bg-clip-padding
        border border-solid border-gray-300
        rounded
        transition
        ease-in-out
        m-0
        focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" id="State"
        v-model="user.state"
        placeholder="State">
    </div>



    <div class="form-group mb-6">
      <label for="exampleInputPassword1" class="form-label inline-block mb-2 text-gray-700">Gender</label>
      <input type="Gender" class="form-control block
        w-full
        px-3
        py-1.5
        text-base
        font-normal
        text-gray-700
        bg-white bg-clip-padding
        border border-solid border-gray-300
        rounded
        transition
        ease-in-out
        m-0
        focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" id="Gender" v-model="user.gender"
        placeholder="Gender">
    </div>

    <div class="form-group form-check mb-6">
      <input type="checkbox"
        class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer"
        id="exampleCheck1">
      <label class="form-check-label inline-block text-gray-800" for="exampleCheck1">Terms and Conditions</label>
    </div>
    <button type="submit" class="
      px-6
      py-2.5
      bg-red-600
      text-white
      font-medium
      text-xs
      leading-tight
      uppercase
      rounded
      shadow-md
      hover:bg-blue-700 hover:shadow-lg
      focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0
      active:bg-blue-800 active:shadow-lg
      transition
      duration-150
      ease-in-out" v-on:click="submitValues()">Submit</button>
  </form>

  <td >
                <table class="list" id="employeeList" >
                    <thead>
                        <tr class="border-2 border-black">
                            <th class="border-2 border-black p-2">Name</th>
                            <th class="border-2 border-black p-2">Email</th>
                            <th class="border-2 border-black p-2">Phone</th>
                            <th class="border-2 border-black p-2">State</th>
                                                        <th class="border-2 border-black p-2">Gender</th>

                           <!-- <th class="border-2 border-black p-2">Edit</th>
                            <th class="border-2 border-black p-2">Delete </th> -->
                            
                        </tr>
                        <tr v-for="item in users" :key="item">
                         <td>{{item.name}}</td>
                          <td>{{item.email}}</td>
                           <td>{{item.phone}}</td>
                            <td>{{item.state}}</td>
                                                        <td>{{item.gender}}</td>

                        </tr>
                    </thead>
                    <tbody>

                    </tbody>
                </table>
            </td> 
</div></div></section>




<footer class="p-4 bg-white rounded-lg shadow md:flex md:items-center md:justify-between md:p-6 dark:bg-red-600">
    <span class="text-sm text-white sm:text-center dark:text-white">© 2022 <a href="https://flowbite.com/" class="hover:underline">Flowbite™</a>. All Rights Reserved.
    </span>
    <ul class="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-white sm:mt-0">
        <li>
            <a href="#" class="mr-4 hover:underline md:mr-6 ">About</a>
        </li>
        <li>
            <a href="#" class="mr-4 hover:underline md:mr-6">Privacy Policy</a>
        </li>
        <li>
            <a href="#" class="mr-4 hover:underline md:mr-6">Licensing</a>
        </li>
        <li>
            <a href="#" class="hover:underline">Contact</a>
        </li>
    </ul>
 
</footer>





  



    </div>

</template>

<script>

export default {
 name:"index",
 data(){
  return{
    users:[],
    user:{
      name:'',
      email:null,
      phone:null,
      state:null,
      gender:null
    }
  }
 },
 methods:{
   submitValues(){
    

    console.log("submit"),
    this.users.push(this.user);
    console.log(this.user)
  }
 }
}
</script>












