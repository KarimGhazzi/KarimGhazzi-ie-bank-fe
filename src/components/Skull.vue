<template>
    <div class="bank-skull">
        <h1>Skull</h1>
        <p>Environment variables read from file {{ env_var_file_name }}</p>
        <p>{{ msg }}, and it is running from the {{ environment }} environment</p>
        <button type="button" class="btn btn-secondary">
            Skull button
        </button>
        <nav class="bank-nav">
        <ul>
          <li><router-link to="/">Return to homepage</router-link></li>
          <li><router-link to="/accounts">Go to Accounts</router-link></li>
        </ul>
    </nav>
  </div>
</template>
 
<script>
import axios from 'axios'
export default
    {
        name: 'Skull',
        data() {
            return {
                msg: 'Hi! This is the skull component 💀'
            }
        },
        methods:
        {
            getSkull() {
                const path = `${process.env.VUE_APP_ROOT_URL}/skull`;
                axios.get(path)
                    .then((response) => {
                        this.msg = response.data;
                        this.environment = process.env.NODE_ENV;
                        this.env_var_file_name = process.env.VUE_APP_ENV_VAR_FILE_NAME
                    })
                    .catch(error => console.log(error))
            }
        },
        created() {
            this.getSkull()
        }


    }
    function goback(){

    }
</script>
<style scoped>
.bank-skull {
  background-color: #0074e4;
  color: #ffffff;
  font-family: Arial, sans-serif;
  text-align: center;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.bank-header {
  padding: 20px;
}

.bank-nav ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.bank-nav li {
  margin: 10px;
}

.bank-nav a {
  text-decoration: none;
  color: #ffffff;
  font-weight: bold;
  font-size: 18px;
}

.bank-footer {
  padding: 10px;
  background-color: #0050a7;
}
</style>
