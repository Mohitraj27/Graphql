# lco-graphql

# Request Payload
mutation{
  createCourse(input:{
    courseName:"JS Bootcamp"
    price: 199
    stack: MOBILE
    teachingAssists:[
      {
        firstName: "Mohit"
        lastName: "Raj"
        experience: 1
      },
      {
        firstName: "Raj"
        lastName: "kumar"
        experience: 12
      }
    ]
  }){
    id,
    courseName
  }
}


## Response 
{
  "data": {
    "createCourse": {
      "id": "qavAbcI-qVpcUiLz0LBnf",
      "courseName": "JS Bootcamp"
    }
  }
}



# Query for Fecthing
## Request Payload
query{
  getCourse(id:"qavAbcI-qVpcUiLz0LBnf"){
    id
    teachingAssists{
      experience
    }
  }
}

## Response
{
  "data": {
    "getCourse": {
      "id": "qavAbcI-qVpcUiLz0LBnf",
      "teachingAssists": [
        {
          "experience": 1
        },
        {
          "experience": 12
        }
      ]
    }
  }
}

