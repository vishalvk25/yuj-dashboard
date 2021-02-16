<template>
     <div class="common-card">
          <b>{{listTitle}}</b>
          <select >
            <option>By sessions</option>
          </select>
            <div class="prog-main" v-for="(list,index) in ListData" :key="list">
              <div class="prog-section">
                <label class="custom-label">{{list}}</label>
                <div class="progress">
                  <div class="progress-bar" style="width:70%; "></div>
                </div>
              </div>
              <div class="prog-label">
                  {{listcount[index]}}
              </div>
            </div>
          </div>

</template>

<script>
export default {
  name: 'List',
  props: ['ListData','listTitle','listcount'],
  data() {
      return {
        listd: ['314k']
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dashboard-main{
  padding: 10px;
  background-color: #262626;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.pr-o{
  padding-right: 0;
}
.pl-o{
  padding-left: 0;
}
.card{
  border-radius: 0rem !important;
}
.bg-dark-1{
  background-color: #0f0f0f;
}
.bg-dark-2{
  background-color: #181818;
}
.common-card{
  color: #ffffff;
  text-align: left;
}
select {
    background: no-repeat;
    color: #fff;
    padding-right: 10px;
    border: 0;
    border-bottom: 1px solid;
}
.progress,.progress-bar {
    height: 1px!important;
}
.prog-section{
    width: 65%;
    display: inline-block;
    float: left;
}
.prog-label{
    width: 35%;
    display: inline-block;
    float: left;
    padding: 20px 0px 0px 10px;
}
.custom-label{
      margin-bottom: 0;
      font-size: 11px;
      margin-top: 10px;
}
</style>
