<template>
    <div id="crud">
        <div>this is render by CRUD!!</div>
        <div v-for="property in obj">
          <template v-if="property.type == 'string'">
            {{property.name}} : <input name="{{property.name}}" type="text" value="str" v-model="value[property.name]"/>
          </template>
          <template v-if="property.type == 'number'">
            {{property.name}} : <input name="{{property.name}}" type="text" value="3" v-model="value[property.name]"/>
          </template>
        </div>
    </div>
</template>
<style>

</style>

<script>

    export default{
        data(){
            return{
                obj:[
                    {
                      "name": "title",
                      "type": "string",
                      "rule":"NOT_NULL"
                    },
                    {
                      "name": "artist",
                      "type": "string",
                      "rule": "NOT_NULL"
                    },
                    {
                      "name": "sales",
                      "type": "number",
                      "rule": "NOT_NULL"
                    }
                  ],
            value:{}
            }
        },
        components:{

        }
    }
</script>
