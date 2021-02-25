---
title: xpath 사용해서 엘리먼트 찾기
date: 2020-03-31 23:38:45
tags:
---

1. xpath에 엘리먼트가 로딩(?) 될 때 까지 5초 기다림.
엘리먼트가 로드되면 esc 누름. 외국서버에 있는 홈페이진데 굳이 모든 요소가 로딩될때까지 기다릴 필요는 없으니 ㅇㅇ
~~~
WebDriverWait(driver, 5).until(
EC.presence_of_element_located((By.XPATH , """ // *[@id="mainContent"]/div/div[1]/main/div[1]/div[1]/p """))
)
ActionChains(driver).send_keys(Keys.ESCAPE).perform()
~~~
2. 지정한 위치(xpath)에 있는 요소를 찾음. 그리고 걔를 num_of_results라는 변수로 저장. 
~~~
num_of_results= driver.find_element_by_xpath(""" //*[@id="mainContent"]/div/div[1]/main/div[1]/div[1]/p """)
~~~
3. 2번과 같이 xpath로 엘리먼트를 찾아서 info라고 정의.
~~~
info = driver.find_element_by_xpath("""//*[@id="product-description-content-8"]/div/div""")
~~~
4. info라는 엘리먼트 내부(.)에서 p태그를 가진 요소'들'을 모두 찾음(//p). elements이기 때문에 serving_info는 리스트임. ㅇㅇ.

~~~        
serving_info=info.find_elements_by_xpath(".//p")
~~~

5. info라는 엘리먼트 내부의 테이블을 모두 찾는데(.//table) 그 테이블이 td의 child일 경우에는 제외([not(ancestor::td)])
~~~
nutritional_info=info.find_elements_by_xpath(""".//table[not(ancestor::td)]""")
~~~
6. table이라는 엘리먼트 내부의 td태그를 가진 요소들을 모두 찾는데, 그 td가 table을 child로 가지는 경우에는 제외 ([not(child::table)])
~~~
nut_info_text = table.find_elements_by_xpath(""".//td[not(child::table)]""")
~~~