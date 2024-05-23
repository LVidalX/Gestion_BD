Base de datos Eventos

Script DDL 
CREATE TABLE events (
     id SERIAL PRIMARY KEY,
     description TEXT,
     events_date DATE,
     city VARCHAR(75),
     total_assistants INT     
);

CREATE TABLE conferences (
     id SERIAL PRIMARY KEY,
     title VARCHAR(100),
     speaker VARCHAR(60),
     hour TIME,
     congress_day DATE,
     event_id INT,
     FOREIGN KEY (event_id) REFERENCES events(id)
);

CREATE TABLE members (
     id SERIAL PRIMARY KEY,
     name VARCHAR(75),
     last_name VARCHAR(50),
     email VARCHAR(150)
);

CREATE TABLE _record (
     id SERIAL PRIMARY KEY,
     member_id INT,
     conference_id INT,
     assistance_date DATE,
     assistance VARCHAR(12),
     FOREIGN KEY (member_id) REFERENCES members(id),
     FOREIGN KEY (conference_id) REFERENCES conferences(id)
);


Sentencias 
![image](https://github.com/LVidalX/Gestion_BD/assets/116664703/9ed828f9-2769-46de-926b-b716a80a8cd2)

![image](https://github.com/LVidalX/Gestion_BD/assets/116664703/52f52512-119b-44b4-90ab-eab9b31e807e)

![image](https://github.com/LVidalX/Gestion_BD/assets/116664703/98f8788c-e7ac-460a-9edf-9c183d7bae3b)

![image](https://github.com/LVidalX/Gestion_BD/assets/116664703/ac46b7c1-b23a-437f-baaf-f32240379553)

![image](https://github.com/LVidalX/Gestion_BD/assets/116664703/46e44314-d31e-47c3-b961-e2fa1cc1e5ed)




