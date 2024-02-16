1) Create datebase with the following name `task`
2) Open backend source inside of this there is config folder,there is app-data-source.ts file, here update the database credentials
3) Now need to install node dependencies, on backend,
4) Run the following command for generate migration file, npm run typeorm:generate-migration
5) Once above command successfully executed, you can see migration file inside of config folder, we need to replace this config file inside of config/migrations folder,
6) Generated migration file need to write on our db so run following command `npm run typeorm -- -d ./src/config/app-data-source.ts migration:generate ./src/config/migrations/`
7) Now you are ready to start the backed server
8) Once the backend server is running successfully,
9) Get the server API URL from console, and update this in frontend .env file REACT_APP_API_BASE_URL key,
10) Install frontend dependencies from front end root path, using npm install command,
11) Once everything installed, run frontend on dev server using npm run dev,
12) Now need to create sample user for launch to dashboard, use HTTP reqeust handler POSTMAN :
```
      create users
      API URL :http://localhost:8005/api/users
      {
            "firstName": "Dhilip",
            "lastName":"Kumar",
            "gender": "Male",
            "phoneNo": "8120452221",
            "email": "ramkumar@gmail.com",
            "password":"Colan@12",
            "dob": "07/08/1997",
        		"address":[{
                "street": "Railar nagar",
                "city": "Madurai",
                "state": "Tamil Nadu",
               "postalCode": "625018",
                "country": "India" 
              }]
      }
```

with above created user's email and password can able to authenticate the login page
