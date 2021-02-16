<template>
<div class="dashboard-main">
  <div class="row">
      <div class="col-md-6">
            <div class="row">
                <div class="col-md-6 pr-o">
                  <div class="card bg-dark-1">
                    <div class="card-body">
                       <div class="common-card">
                       <b> CPU Utilization </b>
                        <select class="float-right">
                          <option>All Alerts</option>
                        </select>
                        <bar-chart></bar-chart>
                       </div>

                       <h1><hr/></h1>
                       <div class="common-card">
                       <b> Sessions </b>
                        <div class="float-right">
                          213<small> / Minutes</small>
                        </div>
                       </div>
                    </div>
                  </div>
                </div>
                <div class="col-md-3">
                    <div class="card bg-dark-1">
                    <div class="card-body">
                        <div class="common-card">
                           <b>Application Risk Level</b>
                        </div>
                    </div>
                  </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                    <div class="card bg-dark-2">
                    <div class="card-body">
                        <List v-bind:ListData="listdata3" v-bind:listTitle="listTitle3" v-bind:listcount="listcount3"></List>
                    </div>
                  </div>
                </div>
          </div>
    </div> 
    <div class="col-md-6">
            <div class="row">
                <div class="col-md-3 pl-o pr-o">
                    <div class="card bg-dark-2">
                      <div class="card-body"> 
                        <List v-bind:ListData="listdata4" v-bind:listTitle="listTitle4" v-bind:listcount="listcount4"></List>
                      </div>
                    </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                      <div class="card bg-dark-2">
                      <div class="card-body">
                         <List v-bind:ListData="listdata5" v-bind:listTitle="listTitle5" v-bind:listcount="listcount5"></List>
                         </div>
                    </div>
                </div>
                <div class="col-md-6">
                            <div class="card bg-dark-1">
                            <div class="card-body">
                              <div class="common-card">
                                    <b>System Alerts (Last 5)</b> <a class="text-orange">View All</a>
                                    <select class="float-right">
                                      <option>All Alerts</option>
                                    </select>
                              <div class="row">
                                <div class="col-md-12">
                                  <div class="card bg-dark-2">
                                   <div class="card-body">
                                    <small>asfasf sfasfasf</small> <a class="pull-right text-orange">View Details</a>
                                    <p>asf asfasfasafs </p>
                                  </div>
                              </div>
                            </div>
                            </div>
                          </div>
                        </div>
                      </div>
                </div>
          </div>
    </div>
</div>
 <div class="row pt-3">
      <div class="col-md-6">
            <div class="row">
                <div class="col-md-3">
                         <div class="card bg-dark-2">
                            <div class="card-body">
                              <List v-bind:ListData="listdata6" v-bind:listTitle="listTitle6" v-bind:listcount="listcount6"></List>
                              <hr/>
                               <List v-bind:ListData="listdata7" v-bind:listTitle="listTitle7" v-bind:listcount="listcount7"></List>
                              </div>
                          </div>
                </div>
                <div class="col-md-3">
                    <div class="card bg-dark-1">
                      <div class="card-body">
                        <div class="common-card">
                           <b>Insights</b>
                        </div>
                      </div>
                    </div>
                </div>
                <div class="col-md-3">
                      <div class="card bg-dark-2">
                        <div class="card-body">
                        <div class="common-card">
                           <b>Observed Threats</b>
                        </div>
                        </div>
                      </div>
                </div>
                <div class="col-md-3 pr-o">
                    <div class="card bg-dark-1">
                      <div class="card-body">Basic card</div>
                    </div>
                </div>
          </div>
    </div> 
    <div class="col-md-6">
            <div class="row">
                <div class="col-md-3 pl-o">
                           <div class="card bg-dark-1">
    <div class="card-body">Basic card</div>
  </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                            <div class="card bg-dark-2">
    <div class="card-body">
          <List v-bind:ListData="listdata" v-bind:listTitle="listTitle" v-bind:listcount="listcount"></List>
    </div>
  </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                    <div class="card bg-dark-2">
                      <div class="card-body">
                         <List v-bind:ListData="listdata1" v-bind:listTitle="listTitle1" v-bind:listcount="listcount1"></List>
                      </div>
                    </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                    <div class="card bg-dark-2">
                      <div class="card-body">
                     <List v-bind:ListData="listdata2" v-bind:listTitle="listTitle2" v-bind:listcount="listcount2"></List>
                      </div>
                  </div>
                </div>
          </div>
    </div>
</div>
</div>
</template>

<script>
import List from './List.vue'
import BarChart from './Charts/BarChart';
export default {
  name: 'Dashboard',
  props: {
    msg: String
  },
  components:{
    List
  },
  data() {
      return {
        tableData: {
            name: 'Facebook',
            visitors: '1,480',
            progress: 60,
            progressType: 'gradient-danger',
          },
          listTitle: 'Top Viruses',
          listdata: ['Torjan Horse','Power Worm','Mydoom','StormWorm','Brain'],
          listcount: ['43','41','35','34','20'],

          listTitle1: 'Top Instrusions',
          listdata1: ['EchoReply','SSLv2.0...Hello2','OpenVPN...closure','DNSquery...com','1.0.345.6'],
          listcount1: ['9.14k','130','6','1','1'],

          listTitle2: 'Top Botnets',
          listdata2: ['98.234.167.228','192.268.2.345','75.75.812.09','1.0.345.6','87.13.187.01'],
          listcount2: ['45 GB','24 GB','21 GB','12 GB','9 GB'],

          listTitle3: 'Top Applications',
          listdata3: ['General HTTPS','General DNS','General UDP','General H_S MGMT','General HTTP'],
          listcount3: ['435 k','412 k','353 k','341 k','204 k'],

          listTitle4: 'Top Addresses',
          listdata4: ['75.75.812.09','98.234.167.228','18.13.187.01','192.268.2.345','1.0.345.6'],
          listcount4: ['45 k','45 k','45 k','45 k','45 k'],

          listTitle5: 'Top Users',
          listdata5: ['Admin','Admin 2','Unknown','Supervisor','Unknown'],
          listcount5: ['45 GB','41 GB','24 GB','18 GB','5 GB'],

          listTitle6: 'Policies  Security Rules',
          listdata6: ['Allowed','Discarded','Dropped'],
          listcount6: ['90 %','8 %','2 %'],
          
          listTitle7: 'NAT Rules',
          listdata7: ['Translation','Non-Translation'],
          listcount7: ['63 %','37 %'],
      
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
    height: 8px!important;
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
.text-orange{
  color: #d76924;
}
</style>
