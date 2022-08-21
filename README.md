# dependency-injector-fastapi
app/application.py => app dari fastapi (second top after __init__.py)
app/giphy.py => api dari giphy (https://api.giphy.com/v1)
app/endpoints.py => url
app/services.py => logical business
app/containers.py => dependency injection (kumpulan dari provider)
app/tests.py => integration test

<br>

alur<br>
user mengunjungi web => masuk ke application.py => mengakses url dlm file endpoints.py & mengakses juga containers (provider yg diperlukan) => after access endpoints run func index => func index need services.py => services.py need giphy api from giphy.py. if need another data like environment variable will accessing containers.py (config.yml) 

# WHEN RUN , APP IS ERROR. DIDNT KNOW ISSUE