<template>
  <Appheader />

  <section>
    <div>
      
      <div class="text-center font-bold text-2xl mt-5"><p>SUMMARY AND CHECKOUT PAGE</p></div>

      <div class="text-center text-xl font-bold">ESTIMATIONS</div>

      <div v-show="currentstep === 1" class="bg-white h-full mt-10 font-semibold">
        <form class="flex sm:px-4 md:px-10 lg:px-96">
          <div class="w-full">
            <div class="flex justify-between">
              <div>
                <label class="">Your Order</label>
              </div>
              <input class="rounded border-black border h-8 w-7/12 
                focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500" type="text" 
                v-model="summary.order"
              >
            </div>
            <div class="flex justify-between mt-3">
              <div>
                <label class="">Quantities</label>
              </div>
              <input class="rounded border-black border h-8 w-7/12
                focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500" type="number" 
                v-model="summary.quantity"
              >
            </div>
              <div class="flex justify-between mt-3">
              <div>
                <label class="">Price</label>
              </div>
              <input class="rounded border-black border h-8 w-7/12
                focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500" type="text" 
                v-model="summary.price"
              >
            </div>
          </div>
          </form>
          <div class="mr-5 text-center">
              <button class="border border-red-600 shadow-md text-gray-600 h-11 mr-2 px-2 py-1 w-28 rounded font-bold mt-6" @click.prevent="prev()">BACK</button>
              <button class="bg-green-600 shadow-md h-11 mr-2 text-white px-2 py-1 w-28 rounded font-bold mt-6" @click.prevent="next()">CHECKOUT</button>
          </div>
        </div>

    </div>
  </section>

  <Appfooter />
</template>

<script>
import Appheader from '../components/Allheader';
import Appfooter from '../components/Allfooter';
export default {
  components:{Appheader, Appfooter},
  data(){
    return{
      currentstep:1,
      summary:[
        {order:'', quantity:'', price:''}
      ]
    }
  }
}
</script>

<style>

</style>