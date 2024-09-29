# tietokannat
moduuli 3
1. SELECT * 
    -> FROM goal;
<img width="794" alt="Screenshot 2024-09-28 at 12 18 26" src="https://github.com/user-attachments/assets/3e3c7eb6-7b66-4be2-b095-453a8328832e">

2. select name from airport where iso_country = "FI";
<img width="354" alt="Screenshot 2024-09-28 at 13 06 01" src="https://github.com/user-attachments/assets/52f47e8c-7631-4aef-ac1d-09f0bab4b855">

3. select name from airport where iso_country = "FI" order by name;
<img width="339" alt="Screenshot 2024-09-28 at 13 08 27" src="https://github.com/user-attachments/assets/d804ec11-e149-4c1b-a7c0-32f0bc0eff5f">

4. select name, `type` from airport where iso_country = "FI" order by type, name;
<img width="1440" alt="Screenshot 2024-09-28 at 13 10 20" src="https://github.com/user-attachments/assets/c4b7568e-7bad-4f8c-b745-b96f8a3ab6a0">
<img width="1440" alt="Screenshot 2024-09-28 at 13 10 25" src="https://github.com/user-attachments/assets/511e61e1-7af1-47df-9f83-5d3ed7a00a94">

5. select name from country where name like "F%";
 <img width="326" alt="Screenshot 2024-09-28 at 13 12 10" src="https://github.com/user-attachments/assets/54f0103a-327b-4dc5-97b0-7cf5775e8408">

6. select name from country where name like "%F%";
<img width="268" alt="Screenshot 2024-09-28 at 13 13 50" src="https://github.com/user-attachments/assets/d0ea519b-8e4d-4a50-b166-c117942f6651">

7. select location from game where screen_name = "Vesa";
<img width="211" alt="Screenshot 2024-09-28 at 13 16 09" src="https://github.com/user-attachments/assets/1894ce4e-b884-4d38-bd57-28f7b5d12fdf">

8. select co2_consumed from game where screen_name = "Ilkka";
<img width="137" alt="Screenshot 2024-09-28 at 13 17 46" src="https://github.com/user-attachments/assets/a32d99e1-c63b-4378-84e3-6e4b583ed2cb">

9. select distinct co2_budget from game;
<img width="125" alt="Screenshot 2024-09-28 at 13 19 47" src="https://github.com/user-attachments/assets/2509f19a-abf5-4c10-a110-963342aba492">


moduuli 4

1. select country.name as "country name", airport.name as "airport name"
    -> from airport, country
    -> where airport.iso_country = country.iso_country and country.name = "Iceland";
<img width="349" alt="Screenshot 2024-09-28 at 14 04 53" src="https://github.com/user-attachments/assets/7fdad425-c1c4-484d-baeb-278fd7b282e0">

2. select airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";
<img width="585" alt="Screenshot 2024-09-28 at 14 06 34" src="https://github.com/user-attachments/assets/20f50645-6161-4397-97b9-ae75bd7e6bf0">

3. select country.name as country_name, airport.name as airport_name
from airport, country
where airport.iso_country = country.iso_country and country.continent = "AN";
<img width="617" alt="Screenshot 2024-09-28 at 14 09 03" src="https://github.com/user-attachments/assets/48146cc3-fefb-4a98-8d59-828ab00f7424">

4. select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
<img width="190" alt="Screenshot 2024-09-28 at 14 10 54" src="https://github.com/user-attachments/assets/fc97ac6a-1ffa-4b5c-acc4-9a6db0525bfb">

5.select elevation_ft * 0.3048 as elevation_m
    -> from airport, game
    -> where location = ident and screen_name = "Heini";
    <img width="131" alt="Screenshot 2024-09-28 at 14 12 27" src="https://github.com/user-attachments/assets/d93dee35-712e-4d43-9d81-3258c4dbfa7a">

6.select name
from airport, game
where location = ident and screen_name = "Ilkka";
<img width="195" alt="Screenshot 2024-09-28 at 14 14 12" src="https://github.com/user-attachments/assets/0552afcd-9903-498e-a1a3-44f357fca52d">

7. select country.name
from airport, game, country
where location = ident and airport.iso_country = country.iso_country  and screen_name = "Ilkka";
<img width="149" alt="Screenshot 2024-09-28 at 14 43 57" src="https://github.com/user-attachments/assets/77e2d70a-05fd-4396-b004-2b1ad4cacad3">

8.select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
<img width="89" alt="Screenshot 2024-09-28 at 14 45 46" src="https://github.com/user-attachments/assets/0a0587e6-fb94-4b9c-a200-ca9b3c32fa00">

9.select airport.name
from airport, game, goal, goal_reached
where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
<img width="199" alt="Screenshot 2024-09-28 at 14 47 50" src="https://github.com/user-attachments/assets/628d98da-07fe-44f5-bfe6-8e92f0371261">

10 .select country.name
from country, airport, game, goal, goal_reached
where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
<img width="139" alt="Screenshot 2024-09-28 at 14 48 58" src="https://github.com/user-attachments/assets/455d97ef-fd32-4c82-8b10-1b0e1e670d68">

moduuli 5
1. select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";
<img width="333" alt="Screenshot 2024-09-29 at 12 44 21" src="https://github.com/user-attachments/assets/7aaa0d38-5cd0-4337-b259-4ac2f962f79d">

2.select screen_name, airport.name
from game inner join airport on location = ident;
<img width="300" alt="Screenshot 2024-09-29 at 12 45 35" src="https://github.com/user-attachments/assets/4981b10b-acf3-48b2-8651-e8016c345d1d">

3.select screen_name, country.name
from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;
<img width="311" alt="Screenshot 2024-09-29 at 12 46 54" src="https://github.com/user-attachments/assets/ae80cac4-32b3-4bdb-9cf7-9eba324f6b96">

4.select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";
<img width="413" alt="Screenshot 2024-09-29 at 12 48 35" src="https://github.com/user-attachments/assets/2c694a4d-52a4-4b42-834e-70473f1f8117">

5. select name, screen_name
from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;
<img width="176" alt="Screenshot 2024-09-29 at 12 49 45" src="https://github.com/user-attachments/assets/d9affd6d-24c1-4c1e-9478-4efe128ec028">

moduuli 6
1. select name
from country
where iso_country in(
select iso_country
from airport
where name like "Satsuma%"
);
<img width="97" alt="Screenshot 2024-09-29 at 13 14 06" src="https://github.com/user-attachments/assets/f9bdbb55-9569-4e7b-b354-0c3a90422999">

2.select name
from airport where
iso_country in(
select iso_country
from country
where name = "Monaco"
);
<img width="272" alt="Screenshot 2024-09-29 at 13 15 41" src="https://github.com/user-attachments/assets/ab15aeb1-f01a-489f-90f8-a4f886d98685">

3. select screen_name
from game
where id in (
select game_id
from goal_reached
where goal_id in(
select id
from goal
where name = "CLOUDS"
)
);
<img width="118" alt="Screenshot 2024-09-29 at 13 16 34" src="https://github.com/user-attachments/assets/802a58a1-0e8a-4e93-9ddf-38af466fd8de">

4.select country.name
from country
where iso_country not in
(select airport.iso_country
from airport);
<img width="243" alt="Screenshot 2024-09-29 at 13 18 34" src="https://github.com/user-attachments/assets/1f0210c6-edac-4e6b-8dc0-c6eab206a70e">

5.select name
from goal
where id not in(
select goal.id
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini"
);
<img width="76" alt="Screenshot 2024-09-29 at 13 19 37" src="https://github.com/user-attachments/assets/e7db14b6-87cb-4072-a1bd-138d7e4ca914">

moduuli 7

1. select max(elevation_ft)
from airport;
<img width="162" alt="Screenshot 2024-09-29 at 16 14 03" src="https://github.com/user-attachments/assets/56885de6-7cd4-4bc7-8604-f2bca3c75a3a">

2.select continent, count(*)
from country
group by continent;
<img width="164" alt="Screenshot 2024-09-29 at 16 14 57" src="https://github.com/user-attachments/assets/df9a5490-b34c-4283-aba5-31a592d27b13">

3.select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;
<img width="185" alt="Screenshot 2024-09-29 at 16 17 33" src="https://github.com/user-attachments/assets/dff41c32-dad8-47be-b2a6-2d18536f30ef">

4.select screen_name
from game
where co2_consumed in(
select min(co2_consumed)
from game
);
<img width="115" alt="Screenshot 2024-09-29 at 16 18 29" src="https://github.com/user-attachments/assets/0d3cbcf3-78f5-4992-a56d-b05da8c74b8e">

5.select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;
<img width="248" alt="Screenshot 2024-09-29 at 16 20 20" src="https://github.com/user-attachments/assets/b677bae3-6d8a-425f-ab04-6de594c69f34">

6.select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;
<img width="120" alt="Screenshot 2024-09-29 at 16 21 51" src="https://github.com/user-attachments/assets/0d44aa9f-642b-4e62-9338-787f72e4e4c6">

7.select name
from airport
where elevation_ft in (
select max(elevation_ft)
from airport
);
<img width="220" alt="Screenshot 2024-09-29 at 16 36 07" src="https://github.com/user-attachments/assets/d238c853-4630-428e-a5f7-baac565ce36c">

8.select name
from country
where iso_country in (
select iso_country
from airport
where elevation_ft in(
select max(elevation_ft)
from airport
)
);
<img width="61" alt="Screenshot 2024-09-29 at 16 37 06" src="https://github.com/user-attachments/assets/24b6093a-0dd4-4507-9c96-6883d491053f">

9.select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;
<img width="78" alt="Screenshot 2024-09-29 at 16 38 37" src="https://github.com/user-attachments/assets/52b3be89-3365-4f32-8f63-786def9b9638">

10.select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);
<img width="204" alt="Screenshot 2024-09-29 at 16 39 52" src="https://github.com/user-attachments/assets/a0564c0d-fe5c-4506-94ed-be510f7665e1">


