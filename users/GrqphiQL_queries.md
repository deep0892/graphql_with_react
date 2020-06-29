# query fetcUser{

# user(id:"23"){

# id,

# firstName,

# age,

# company {

# id,

# name,

# description

# }

# }

# }

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
