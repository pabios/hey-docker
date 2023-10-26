docker-compose build
docker-compose up -d

#
docker exec -it pabiosfile bash

#
symfony new pabios-first --full
cd pabios-first
symfony serve -d

# bdd
adduser pabios
  => mdp = pass

# 
 > chown: changing ownership of './.git/objects/8b/d9061d53c8d3913bbb31cc42a41726e128492f': Permission denied

chown pabios:pabios -Rf .  [on le force]

#
symfony console make:entity
symfony console make:migration
symfony console doctrine:migrations:migrate

#
composer require annotations
symfony console make:crud
#
run http://localhost:9000/user/ and enjoy 😍


## thanks to lefevre djim 
 
