# az-env-loader
A simple package to get azure secrets from key vault and load it to proccess.env


# Sample Usage
````
let { loadEnv } = require('az-env-loader')
let dotenv = require('dotenv')
dotenv.config()

// extra step when compared to normal loading of env
loadEnv().then(res=>{
    console.log("loaded all Azure Valut Env's")

})
````




# sample .env file 
````
SECRET=@msvault(<your-secret-url-here>)
````

# Secret URL Format

your secret url should be of the format 
````
https://<YOUR-KEY-VAULT-URL>/secrets/<secret-name>
````