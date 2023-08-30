__Добавление объявления в избранное__
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
import time
driver = webdriver.Chrome()

#Открытие страницы с объявлением
driver.get("https://www.avito.ru/nikel/knigi_i_zhurnaly/domain-driven_design_distilled_vaughn_vernon_2639542363")

#Добавление объявления в избранное
time.sleep(5) #Подождать несколько секунд, чтобы элементы загрузились
favorites_button = driver.find_element(By.CSS_SELECTOR, "button[class*= desktop-usq1f1]")
favorites_button.click()

#Проверка объявления в избранном
time.sleep(5)#Подождать несколько секунд, чтобы элементы загрузились
favorite_link = driver.find_element(By.CSS_SELECTOR, "a[class*= index-counter-UxPCj]")
favorite_link.click()

#Закрытие браузера
driver.quit()
```
