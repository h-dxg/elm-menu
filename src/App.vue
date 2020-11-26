<template>
  <div id="app">
    <img
      alt="Vue logo"
      src="./assets/logo.png"
    />
    <Menu :router="menuList"> </Menu>
  </div>
</template>

<script>
import Menu from "./components/menu.vue";

export default {
  name: "App",
  components: {
    Menu
  },
  data () {
    return {
      menuList: [
        {
          iOrder: 1,
          id: "1",
          image: "",
          name: "基础信息",
          parent: "",
          route: "basicInformation",
          children: [
            {
              iOrder: 0,
              id: "1-1",
              name: "组织框架",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "kzjorganization"
            },
            {
              iOrder: 0,
              id: "1-2",
              name: "角色信息",
              parent: "",
              permitList: [
                {
                  id: "8BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "kzjroleInformation"
            },
            {
              iOrder: 0,
              id: "1-3",
              name: "用户信息",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "kzjuser"
            }
          ]
        },
        {
          iOrder: 2,
          id: "2",
          image: "",
          name: "工厂建模",
          parent: "",
          route: "factoryModel",
          children: [
            {
              iOrder: 0,
              id: "2-0",
              image: "",
              name: "排班策略",
              parent: "",
              route: "",
              children: [
                {
                  iOrder: 0,
                  id: "0-1",
                  name: "班次信息管理",
                  parent: "",
                  permitList: [
                    {
                      id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                      name: "OnBetchLot"
                    }
                  ],
                  route: "sche-shifts"
                }
              ]
            },
            {
              iOrder: 0,
              id: "0-1",
              name: "班次信息维护",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "sche-shifts"
            },
            {
              iOrder: 0,
              id: "0-2",
              name: "班组信息维护",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "sche-team"
            },
            {
              iOrder: 0,
              id: "0-3",
              name: "节假日信息管理",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "sche-holiday"
            },
            {
              iOrder: 0,
              id: "0-4",
              name: "工作日历信息管理",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "sche-work"
            },
            {
              iOrder: 0,
              id: "0-5",
              name: "排班策略管理",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "sche-plan"
            },
            {
              iOrder: 0,
              id: "0-6",
              name: "排班生成列表",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "sche-generate"
            },
            {
              iOrder: 0,
              id: "2-1",
              name: "物料信息",
              parent: "",
              permitList: [
                {
                  id: "7BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "material"
            },
            {
              iOrder: 0,
              id: "2-2",
              name: "生产线设备",
              parent: "",
              permitList: [
                {
                  id: "8BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "productionEquipment"
            },
            {
              iOrder: 0,
              id: "2-3",
              name: "设备台账",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "equipmentAccount"
            },
            {
              iOrder: 0,
              id: "2-4",
              name: "反应釜配置",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "reactionKettle"
            },
            {
              iOrder: 0,
              id: "2-5",
              name: "测量点配置",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "measuringPoint"
            },
            {
              iOrder: 0,
              id: "2-6",
              name: "能源类型配置",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "energyType"
            },
            {
              iOrder: 0,
              id: "2-7",
              name: "能源介质配置",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "energyMedium"
            },
            {
              iOrder: 0,
              id: "2-8",
              name: "能源仪表",
              parent: "",
              permitList: [
                {
                  id: "9BD44683-5907-4357-A40D-50B6CB1CC57C",
                  name: "OnBetchLot"
                }
              ],
              route: "energyMeter"
            }
          ]
        }
      ]
    };
  },
  methods: {}
};
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
</style>
