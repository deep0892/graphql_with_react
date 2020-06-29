query fetchCompany{
apple: company(id:"1"){
...companyDetails,
users{
...userDetails
}
},
google: company(id:"2"){
...companyDetails,
users{
...userDetails
}
}
}

fragment companyDetails on Company{
id,
name,
description
}
fragment userDetails on User{
id,
firstName,
age
}

mutation {
addUser(firstName: "Dips", age: 27) {
id
firstName
age
}
deleteUser(id: "r70QRng") {
id
}
}

editUser(id: "23", firstName: "Dips.", age: 27) {
id,
firstName,
age
}
