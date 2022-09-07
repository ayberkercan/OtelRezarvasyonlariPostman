# OtelRezarvasyonlariPostman
Postman ile otel rezarvasyonu uygulaması

Body 


TokenOlusturma 

{
    "username" : "admin",
    "password" : "password123"
}

CreatBooking

 "lastname" : "Ercan",
    "totalprice" : {{totalprice}},
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2018-01-01",
        "checkout" : "2019-01-01"
    },
    "additionalneeds" : "Breakfast"
}

Tests

GetBooking
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
let response=pm.response.json();
pm.test("totalprice alanı dogru donmeli",function(){
    pm.expect(response.totalprice).is.eql(pm.environment.get("totalprice"))
}) 


UpdateBooking

{
    "firstname" : "James",
    "lastname" : "Brown",
    "totalprice" : 111,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2018-01-01",
        "checkout" : "2019-01-01"
    },
    "additionalneeds" : "Breakfast"
}


PartialUpdateBooking 

{
    "firstname" : "AyberkTest",
    "lastname" : "Brown"
}

DeleteBooking




