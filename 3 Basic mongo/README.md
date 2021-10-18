# NoSQL
Установил монго через докер, при этом для компаса подходящий докерфайл не нашел, поэтому его поставил локально.  
При подключении компаса к монго возникли проблемы, нашел в интернете решение о запуске монго на порту 27018, поэтому использую следующую команду для запуска  
docker run --name mongodb -d -p 27018:27017 mongo  
Компас подключаю по строке   
mongodb://localhost:27018/?readPreference=primary&appname=MongoDB%20Compass&directConnection=true&ssl=false  
В качестве тестовой я взял несколько коллекций, в том числе большую на 5 млн записей по перевозкам Uber:  
https://www.kaggle.com/fivethirtyeight/uber-pickups-in-new-york-city/version/2?select=uber-raw-data-janjune-15.csv
