from selenium import webdriver
from selenium.webdriver.common.by import By
import pandas as pd
import time

options = webdriver.ChromeOptions()
options.add_argument("--headless")
driver = webdriver.Chrome(options=options)

url = "https://elevenlabs.io/app/home"
driver.get(url)
time.sleep(5)

elements = driver.find_elements(By.XPATH, "//div[@class='classe-a-changer']")  # Modifier avec le bon XPath

data = []
for elem in elements:
    text = elem.text.strip()
    data.append([text])

driver.quit()

df = pd.DataFrame(data, columns=["Données"])
df.to_csv("donnees_elevenlabs.csv", index=False, encoding="utf-8")

print("Extraction terminée. Fichier sauvegardé : donnees_elevenlabs.csv")

# Islam Hadri
