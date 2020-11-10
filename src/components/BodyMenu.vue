<template>
  <div class="container">
      
       <p>
      <td><img class="btn" :src="Body1" >
       </td> 
     
     <td> <img class="btn" :src="Body2" >
      </td> 
 
     <td> <img class="btn" :src="Body3" >  
      </td> 

   

      <p>
      <td><img class="btn" :src="Body4" >
    </td> 
     
     <td> <img class="btn" :src="Body5" >
    </td> 
 
     <td> <img class="btn" :src="Body6"    >
     </td> 
    
<p>

       <td><img class="btn" :src="Body7" >
       </td> 
     
     <td> <img class="btn" :src="Body8" >
     </td> 
 
     <td> <img class="btn" :src="Body9"    >
      </td> 
        </div>       
</template>
    
<script>
import Body1 from "../assets/Body/Body1.png";
import Body2 from "../assets/Body/Body2.png";
import Body3 from "../assets/Body/Body3.png";
import Body4 from "../assets/Body/Body4.png";
import Body5 from "../assets/Body/Body5.png";
import Body6 from "../assets/Body/Body6.png";
import Body7 from "../assets/Body/Body7.png";
import Body8 from "../assets/Body/Body8.png";
import Body9 from "../assets/Body/Body9.png";
export default {
  data() {
    return {
      Body1,Body2, Body3, Body4, Body5,Body6, Body7, Body8,Body9
    };
  },
};

</script>

<style scoped>
.btn {
  width: 103%
}

</style>