Create this directories structure:
.
├── docker-compose.yml
├── Dockerfile
├── dump
│ └── myDb.sql
├── sessions
└── www
    └── index.php

    
db backup : docker exec CONTAINERID /usr/bin/mysqldump --no-tablespaces -u USER --password=root DATABASE > myDb.sql

cat myDb.sql | docker exec -i CONTAINERID /usr/bin/mysql -u USER --password=root DATABASE
