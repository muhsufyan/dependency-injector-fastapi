# dependency-injector-fastapi
alur : user mengunjungi url selanjutnya di server fastapi akan menjalankan program<br>
1. app/__init__.py => top level<br>
2. app/application.py => second level, berisi url & func-nya. need containers as dependency injection, and accessing data for config file<br>
3. app/containers.py => config dan di<br>
4. app/services.py => logical business. need redis for<br>
5. app/redis.py  => config redis & redis pooling

## make virtual environment
python -m venv virtualenv<br>
## untuk run
docker-compose build<br>
docker-compose up<br>

## run test
docker-compose run --rm example py.test app/tests.py --cov=fastapiredis