2023/01/18

### ๐งโ๐ปย **๊ธฐ์ ๋ธ๋ก๊น TechBlog** ๐ช

<aside>
๐ก Annotation

</aside>

* ๊ณต๋ถ๋ฅผ ์ํด์ ํ๋ ๋ธ๋ก๊น์ผ๋ก ์๋ชป๋ ์ ๋ณด๊ฐ ์์ ์ ์์ต๋๋ค.

<br><br>

## [ Spring ] Annotation

**๐ฉย Annotation**

---

**ํ๋ก๊ทธ๋จ์๊ฒ ์ถ๊ฐ์ ์ธ ์ ๋ณด๋ฅผ ์ ๊ณตํ๋ ๋ฉํ๋ฐ์ดํฐ**

์ฃผ์๊ณผ ๋น์ทํ๋, ์ ๋ํ์ด์์ ํ๋ก๊ทธ๋จ์๊ฒ ์ ๋ณด ์ ๊ณต

```java
@GetMapping()
public String hello() {
    return "hello";
}
```

1. ์ปดํ์ผ๋ฌ๋ฅผ ํตํด ๋ฌธ๋ฒ ์๋ฌ ์ฒดํฌ
2. ์๋์ผ๋ก ์ฝ๋๋ฅผ ์์ฑ
3. ๋ฐํ์์ ํน์  ๊ธฐ๋ฅ ์คํ

<br><br>

**+ย Annotation ๋์ ์์**

---

1. `@` ์ฌ์ฉํ์ฌ ์ ๋ํ์ด์ ์ ์
2. ์ฌ์ฉํ๊ณ ์ ํ๋ ์ฝ๋ ์์ ๋ฐฐ์น
3. ์ฝ๋ ์คํ ์ค Reflection์ ํตํด ์ถ๊ฐ ์ ๋ณด ํ๋ํ์ฌ ๊ธฐ๋ฅ ์ค์

<br><br>

**+ย Annotation ์ฉ๋**

---

- ๋ฌธ์ํ
- ์ปดํ์ผ๋ฌ ์ฒดํฌ
- ์ฝ๋ ๋ถ์๊ณผ ์๋ ์์ฑ
- ๋ฐํ์ ํ๋ก์ธ์ฑ

<br><br>

**+ย Reflection**

---

๊ตฌ์ฒด์ ์ธ ํด๋์ค ํ์์ ์์ง ๋ชปํ  ๋, ํด๋์ค์ ๋ฉ์๋์ ํ์, ๋ณ์๋ค์ ์ ๊ทผํ  ์ ์๋๋ก ํด์ฃผ๋ ์๋ฐ API

Reflection์ ์ด์ฉํ๋ฉด Annotation์ ์ ์ฉ ์ฌ๋ถ์ ์๋ฆฌ๋จผํธ ๊ฐ์ ์ฝ๊ณ  ์ฒ๋ฆฌํ  ์ ์์

Annotation ์ง์ ๋ง์ผ๋ก๋ ์ํ๋ ํด๋์ค ์ฃผ์ ๊ฐ๋ฅ

<br><br>

๐ฉย **์๋น ๋ต๋ณ**

---

Q. ์ ๋ํ์ด์์ ๋ํด ๋งํด๋ณด์ธ์.

์ ๋ํ์ด์์ด๋ ํ๋ก๊ทธ๋จ์๊ฒ ์ถ๊ฐ์ ์ธ ์ ๋ณด๋ฅผ ์ ๊ณตํ๋ ๋ฉํ๋ฐ์ดํฐ๋ก ์ฃผ์๊ณผ ๋น์ทํ์ง๋ง ์ฃผ์๊ณผ๋ ๋ฌ๋ฆฌ ํ๋ก๊ทธ๋จ์๊ฒ ์ ๋ณด๋ฅผ ์ ๊ณตํฉ๋๋ค. 

๋ํ ์ ๋ํ์ด์์ ์ปดํ์ผ๋ฌ๋ฅผ ํตํด ๋ฌธ๋ฒ ์๋ฌ๋ฅผ ์ฒดํฌํ๊ณ , ์๋์ผ๋ก ์ฝ๋๋ฅผ ์์ฑํ๋ฉฐ, ๋ฐํ์์ ํน์  ๊ธฐ๋ฅ์ ์คํํฉ๋๋ค.

์ ๋ํ์ด์์ ์ฃผ๋ก ๋ฌธ์ํ, ์ปดํ์ผ๋ฌ ์ฒดํฌ, ์ฝ๋ ๋ถ์๊ณผ ์๋ ์์ฑ, ๋ฐํ์ ํ๋ก์ธ์ฑ์ ์ฌ์ฉ๋๋ฉฐ, `@` ์ ํตํด ์ ๋ํ์ด์์ ์ ์ํ์ฌ ์ฌ์ฉํ๊ณ ์ ํ๋ ์ฝ๋ ์์ ๋ฐฐ์นํ๊ณ , ์ฝ๋ ์คํ ์ค์๋ Reflection์ ํตํด ์ถ๊ฐ ์ ๋ณด๋ฅผ ํ๋ํ์ฌ ๊ธฐ๋ฅ์ ์ค์ํฉ๋๋ค.

<br><br>

๐ฉย **์ฐธ๊ณ **

---

๋ธ๋ก๊ทธ

[์ ๋ํ์ด์์ด๋?](https://eatnows.tistory.com/92)

[[Java] ์ฌํ Effective1](https://www.notion.so/Java-Effective1-114975584b77478d87f6e97021370d3c)

<br><br>
