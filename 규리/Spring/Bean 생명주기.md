2023/01/10

### ๐งโ๐ปย **๊ธฐ์ ๋ธ๋ก๊น TechBlog** ๐ช

<aside>
๐ก Bean LifeCycle

</aside>

* ๊ณต๋ถ๋ฅผ ์ํด์ ํ๋ ๋ธ๋ก๊น์ผ๋ก ์๋ชป๋ ์ ๋ณด๊ฐ ์์ ์ ์์ต๋๋ค.

<br><br>

## [ Spring ] **Bean ์๋ช์ฃผ๊ธฐ**

**๐ฉย Bean ์๋ช์ฃผ๊ธฐ**

---

**์คํ๋ง ์ปจํ์ด๋์ ์ํด ์๋ช์ฃผ๊ธฐ ๊ด๋ฆฌ**

์คํ๋ง ์ปจํ์ด๋๊ฐ ๊ฐ๋๋๊ณ  ๋ณธ๊ฒฉ์ ์ผ๋ก ์ฑ์ด ๋์ํ๊ธฐ ์ ์ ํ ๋ฒ, ์คํ๋ง์ด ์ข๋ฃ๋๊ธฐ ์ ์ ํ ๋ฒ ํน์ ํ ๋์์ ์ํํ  ์ ์๋ ์ด๋ฒคํธ ์กด์ฌ

<br>

1. **์คํ๋ง ์ปจํ์ด๋ ์์ฑ**
2. **์คํ๋ง ๋น ์์ฑ**
3. **์์กด ๊ด๊ณ ์ฃผ์**
    
    ์์กด๊ด๊ณ ์ฃผ์(์์ฑ์ ์ฃผ์)์ ํ์์ ๋ณด๋ฅผ ๋ฐ๊ณ  ๋ฉ๋ชจ๋ฆฌ ํ ๋น์ ํตํด ๊ฐ์ฑ ์์ฑ ์ฑ์
    
    ์ด๊ธฐํ๋ ์์ฑ๋ ๊ฐ๋ค์ ํ์ฉํด ์ธ๋ถ ์ปค๋ฅ์์ ์ฐ๊ฒฐํ๋ ๋ฑ ๋ฌด๊ฑฐ์ด ์์ ์ํ
    
    ๋ชํํ๊ฒ ๋ถ๋ฆฌํ๋ ๊ฒ์ด ์ ์ง๋ณด์ ๊ด์ ์์ ์ข์
    
4. **์ด๊ธฐํ ์ฝ๋ฐฑ(EVENT)**
    
    ํ์คํธ๋ก ์ฌ์ฉํ  ๋ฐ์ดํฐ๋ฅผ ์ฑ์ ์ฌ์  ๋์ ์ ์ ๋ฏธ๋ฆฌ ์ ์ฅ
    
5. **์ฑ ๋ณธ์ฐ์ ๋์ ์ํ**
6. **์๋ฉธ์  ์ฝ๋ฐฑ(EVENT)**
    
    ์ฌ๊ณ ์ ๊ฐ๊น๊ฒ ์คํ๋ง์ด ์ข๋ฃ๋๋ ์ํฉ์์ ๋ฐ์ดํฐ๋ฅผ ๋ฐฑ์ํ๋ ๋ฑ์ ๋์ ์ํ
    
7. **์คํ๋ง ์ข๋ฃ**

<br><br>

**+ ์ฌ์ฉ ๋ฐฉ์**

---

1. ํด๋์ค๊ฐ InitializingBean๊ณผ DisposalBean์ ์์๋ฐ์ ํ afterPropertiesSet, destroy ๋ฉ์๋ ๊ตฌํ
    
    โ ์ด๊ธฐํ ์ฝ๋ฐฑ์ afterPropertiesSet์ด, ์๋ฉธ์  ์ฝ๋ฐฑ์ destroy๊ฐ ํธ์ถ
    
2. @Bean ์ ๋ธํ์ด์์ ๋ด์ฅ๋ ์ค์ ๋ฐฉ์์ผ๋ก ๊ฐ๊ฐ initMethod ํ๋์ destroyMethodํ๋์ ์์ฑ๊ณผ ์๋ฉธ์ ์ ์ฉ๋  ๋ฉ์๋๋ช ์ค์ 
    
    ```java
    @Bean(initMethod="start", destroyMethod="end")
    ```
    
3. @PostConstruct, @Predestroy ์ ๋ํ์ด์์ ์ผ๋ฐ์ ์ผ๋ก ๊ฐ์ฅ ๋ง์ด ์ฌ์ฉ๋๋ฉฐ ๊ถ์ฅ๋จ

<br><br>

๐ฉย **์๋น ๋ต๋ณ**

---

Q. ๋น Bean ์๋ช์ฃผ๊ธฐ์ ๋ํด ๋งํด๋ณด์ธ์.

๋น์ ์คํ๋ง ์ปจํ์ด๋์ ์ํด ์๋ช์ฃผ๊ธฐ๊ฐ ๊ด๋ฆฌ๋ฉ๋๋ค. ****

๋น์ ์๋ช์ฃผ๊ธฐ๋ ์คํ๋ง ์ปจํ์ด๋ ์์ฑํ ํ ์คํ๋ง ๋น์ ์์ฑํ๊ณ  ์์กด ๊ด๊ณ ์ฃผ์ํ ํ ์ด๊ธฐํ ์ฝ๋ฐฑ ์ด๋ฒคํธ ๋ฐ์, ์ฑ ๋ณธ์ฐ์ ๋์ ์ํ, ์๋ฉธ์  ์ฝ๋ฐฑ ์ด๋ฒคํธ ๋ฐ์, ์คํ๋ง ์ข๋ฃ ์์๋ก ์งํ๋ฉ๋๋ค.

์คํ๋ง ์ปจํ์ด๋๊ฐ ๊ฐ๋๋๊ณ  ๋ณธ๊ฒฉ์ ์ผ๋ก ์ฑ์ด ๋์ํ๊ธฐ ์ ์ ํ ๋ฒ, ์คํ๋ง์ด ์ข๋ฃ๋๊ธฐ ์ ์ ํ ๋ฒ ํน์ ํ ๋์์ ์ํํ  ์ ์๋ ์ด๋ฒคํธ ์กด์ฌํ๋ฉฐ ์ด๊ธฐํ์ ์๋ฉธ ๋ฉ์๋๋ย **@PostConstruct, @PreDestroy** ์ ๋ํ์ด์์ ์ฌ์ฉํ๋ ๊ฒ์ด ๊ถ์ฅ๋ฉ๋๋ค.

<br><br>

๐ฉย **์ฐธ๊ณ **

---

๋ธ๋ก๊ทธ

[์คํ๋ง ๊ธฐ๋ณธ ์๋ฆฌ 4. ์คํ๋ง Bean์ ์๋ช์ฃผ๊ธฐ](https://velog.io/@zenon8485/%EC%8A%A4%ED%94%84%EB%A7%81-%EA%B8%B0%EB%B3%B8-%EC%9B%90%EB%A6%AC-4.-%EC%8A%A4%ED%94%84%EB%A7%81-Bean%EC%9D%98-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0)

<br><br>
