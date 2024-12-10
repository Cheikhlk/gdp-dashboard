import requests

def get_weather(city, api_key):
    url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}&units=metric&lang=fr"
        response = requests.get(url)
            if response.status_code == 200:
                    data = response.json()
                            temp = data['main']['temp']
                                    description = data['weather'][0]['description']
                                            print(f"La température à {city} est de {temp}°C avec {description}.")
                                                else:
                                                        print("Erreur lors de la récupération des données.")

                                                        # Remplace par ta clé API
                                                        api_key = 'votre_clé_api'
                                                        city = 'Paris'
                                                        get_weather(city, api_key)