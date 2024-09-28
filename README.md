# tietokannat
moduuli 3
SELECT * 
    -> FROM goal;
<img width="794" alt="Screenshot 2024-09-28 at 12 18 26" src="https://github.com/user-attachments/assets/3e3c7eb6-7b66-4be2-b095-453a8328832e">

select name from airport where iso_country = "FI";
<img width="354" alt="Screenshot 2024-09-28 at 13 06 01" src="https://github.com/user-attachments/assets/52f47e8c-7631-4aef-ac1d-09f0bab4b855">

select name from airport where iso_country = "FI" order by name;
<img width="339" alt="Screenshot 2024-09-28 at 13 08 27" src="https://github.com/user-attachments/assets/d804ec11-e149-4c1b-a7c0-32f0bc0eff5f">

select name, `type` from airport where iso_country = "FI" order by type, name;
<img width="1440" alt="Screenshot 2024-09-28 at 13 10 20" src="https://github.com/user-attachments/assets/c4b7568e-7bad-4f8c-b745-b96f8a3ab6a0">
<img width="1440" alt="Screenshot 2024-09-28 at 13 10 25" src="https://github.com/user-attachments/assets/511e61e1-7af1-47df-9f83-5d3ed7a00a94">

 select name from country where name like "F%";
 <img width="326" alt="Screenshot 2024-09-28 at 13 12 10" src="https://github.com/user-attachments/assets/54f0103a-327b-4dc5-97b0-7cf5775e8408">

select name from country where name like "%F%";
<img width="268" alt="Screenshot 2024-09-28 at 13 13 50" src="https://github.com/user-attachments/assets/d0ea519b-8e4d-4a50-b166-c117942f6651">

select location from game where screen_name = "Vesa";
<img width="211" alt="Screenshot 2024-09-28 at 13 16 09" src="https://github.com/user-attachments/assets/1894ce4e-b884-4d38-bd57-28f7b5d12fdf">

select co2_consumed from game where screen_name = "Ilkka";
<img width="137" alt="Screenshot 2024-09-28 at 13 17 46" src="https://github.com/user-attachments/assets/a32d99e1-c63b-4378-84e3-6e4b583ed2cb">

select distinct co2_budget from game;
<img width="125" alt="Screenshot 2024-09-28 at 13 19 47" src="https://github.com/user-attachments/assets/2509f19a-abf5-4c10-a110-963342aba492">
