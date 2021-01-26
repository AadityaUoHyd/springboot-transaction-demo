# springboot-transaction-demo

# POSTMAN postmapping URL : http://localhost:9090/bookFlightTicket

# JSON data for success (fare < 12000), entire transaction have to saved in 2 MySQL DB named - payment_info & passenger_infos

{
  "passengerInfo":{
    "name":"aadi",
    "email":"aadi@gmail.com",
    "source":"Hyd",
    "destination":"Kolkata",
    "travelDate":"27-01-2021",
    "pickUpTime":"2.0 PM",
    "arrivalTime":"5.0 PM",
    "fare":"11000.0"
  },
  "paymentInfo":{
    "accountNo":"acc1",
    "cardType":"CREDIT"
  }
}

# JSON data for exception (fare > 12000), to verify ACID propety and rollback of partial transaction :

{
  "passengerInfo":{
    "name":"aadi1",
    "email":"aadi1@gmail.com",
    "source":"Delhi",
    "destination":"Ranchi",
    "travelDate":"10-01-2021",
    "pickUpTime":"1.0 PM",
    "arrivalTime":"3.0 PM",
    "fare":"25000.0"
  },
  "paymentInfo":{
    "accountNo":"acc1",
    "cardType":"DEBIT"
  }
}
