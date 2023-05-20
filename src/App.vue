<template>
  <div class="container">
    <section class="row justify-content-center ">
        <div class="col-12">
            <h3 class="mb-4">Seçim 2023 Sayaç</h3> 
            <button type="button" class="btn btn-danger" @click="Reset">Yeniden Say !!!</button>
        </div>
        <div class="col-lg-4 mb-4 d-flex align-items-stretch">
            <div class="card w-100">
                <div class="card-header">Recep Tayyip Erdoğan</div>
                <div class="card-body">
                  <div class="text-center">
                      <img src="./assets/rte.jpg" alt="rte" class="img-rounded img-responsive">
                    </div>
                    <span class="material-symbols-outlined" @click="IncreaseRte">
                      add
                    </span>

                    <span class="m1">
                    <span class="material-symbols-outlined" @click="DecreaseRte">
                      remove
                    </span>
                    </span>
                    <p>{{ tayyip }}</p>
                </div>
            </div>
        </div>
        <div class="col-lg-4 mb-4 d-flex align-items-stretch">
            <div class="card  w-100 ">
                <div class="card-header">Kemal KılıçdarOğlu</div>
                <div class="card-body">
                    <div class="text-center">
                      <img src="./assets/kk.jpg" alt="kk" class="img-rounded img-responsive">
                    </div>
                    <span class="material-symbols-outlined" @click="IncreaseKk">
                      add
                    </span>
                    <span class="m1">
                    <span class="material-symbols-outlined" @click="DecreaseKk">
                      remove
                    </span>
                    </span>
                    <p>{{ kilic }}</p>
                </div>
            </div>
        </div>
    </section>
</div>
</template>

<script>

import {ref} from 'vue'
export default {
  name: 'App',
  components: {},
  setup(){
    const kilic=ref(0)
    const tayyip=ref(0)
    function IncreaseRte () {
      tayyip.value++
    }

    function DecreaseRte () {
      tayyip.value--
    }

    function IncreaseKk () {
      kilic.value++
    }

    function DecreaseKk () {
      kilic.value--
    }

    function Reset(){
      kilic.value=0
      tayyip.value=0
    }
    return{kilic,tayyip,IncreaseRte,DecreaseRte,IncreaseKk,DecreaseKk,Reset}
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
  background-color: #2c3e50;
}
img {
  display: block;
  max-width: 100%;
  height: auto;
}
.material-symbols-outlined{
  margin-right: 15px;
}
.material-symbols-outlined:hover{
    color: #08ce29;
    cursor: pointer;
}
.m1 .material-symbols-outlined:hover{
    color: #ce0808;
    cursor: pointer;
}
h3 {
  margin: 0;
  color: white;
}
button {
  float: right;
}
p{
  font-weight: bolder;
}

</style>
