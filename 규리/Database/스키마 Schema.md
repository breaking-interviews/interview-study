2023/01/04

### π§βπ»Β **κΈ°μ λΈλ‘κΉ TechBlog** πͺ

<aside>
π‘ DB - μ€ν€λ§ Schema

</aside>

* κ³΅λΆλ₯Ό μν΄μ νλ λΈλ‘κΉμΌλ‘ μλͺ»λ μ λ³΄κ° μμ μ μμ΅λλ€.

<br><br>

## [ DB ] μ€ν€λ§ Schema

**π©Β μ€ν€λ§**

---

Schema, λ©νλ°μ΄ν° MetaData 

<aside>
π λ°μ΄ν°λ² μ΄μ€λ₯Ό κ΅¬μ±νλ λ°μ΄ν° κ°μ²΄(Entity) + κ°μ²΄μ νΉμ±μ λνλ΄λ μμ±(Attribute)

+ κ°μ²΄ μ¬μ΄μ μ‘΄μ¬νλ κ΄κ³(Relationship) + λ°μ΄ν° μ‘°μ μ λ°μ΄ν° κ°λ€μ΄ κ°λ μ μ½ μ‘°κ±΄ λ±

</aside>

**λ°μ΄ν°λ² μ΄μ€μ κ΅¬μ‘°μ μ μ½μ‘°κ±΄μ κ΄ν μ λ°μ μΈ λͺμΈλ₯Ό κΈ°μ ν κ²**

DB λ΄ λ°μ΄ν°κ° μ΄λ€ κ΅¬μ‘°λ‘ μ μ₯λλμ§λ₯Ό λνλ΄λ λ°μ΄ν°λ² μ΄μ€ κ΅¬μ‘°

<br><br>

**+Β μ€ν€λ§ νΉμ§**

---

1. λ°μ΄ν° μ¬μ (Data Dictionary)μ μ μ₯λ¨
2. νμ€ μΈκ³μ νΉμ ν ν λΆλΆμ ννμΌλ‘μ νΉμ  λ°μ΄ν° λͺ¨λΈμ μ΄μ©ν΄μ λ§λ€μ΄μ§
3. μκ°μ λ°λΌ λΆλ³μΈ νΉμ±μ κ°μ§
4. μΈμ€ν΄μ€μ μν΄ κ·μ 

<br><br>

**+Β μ€ν€λ§ 3κ³μΈ΅**

---

1. μΈλΆ μ€ν€λ§
2. λ΄λΆ μ€ν€λ§
3. κ°λ μ€ν€λ§

<br><br>

**+Β μΈλΆ μ€ν€λ§**

---

μΈλΆ μ€ν€λ§ External Schema = μ¬μ©μ λ·° View

κ°λ³ μ¬μ©μλ€μ μμ₯μμ λ°μ΄ν°λ² μ΄μ€μ λΌλ¦¬μ  κ΅¬μ‘°λ₯Ό μ μν κ²

λμΌν λ°μ΄ν°μ λν΄, μλ‘ λ€λ₯Έ κ΄μ μ μ μν  μ μλλ‘ νμ©

νλμ λ°μ΄ν°λ² μ΄μ€ μμ€νμλ μ¬λ¬κ°μ μΈλΆ μ€ν€λ§κ° μ‘΄μ¬ κ°λ₯νλ©°, νλμ μΈλΆ μ€ν€λ§λ₯Ό μ¬λ¬κ°μ μμ© νλ‘κ·Έλ¨μ΄λ μ¬μ©μκ° κ³΅μ© κ°λ₯

<br><br>

**+Β κ°λ μ€ν€λ§**

---

κ°λ μ€ν€λ§ Conceptual Schema = μ μ²΄μ μΈ λ·° View

λ¬Όλ¦¬μ μΈ κ΅¬νμ κ³ λ €νμ§ μλ λ°μ΄ν°λ² μ΄μ€μ μ μ²΄ μ‘°μ§μ λν λΌλ¦¬μ μΈ κ΅¬μ‘°

κ° λ°μ΄ν°λ² μ΄μ€μλ ν κ°μ κ°λ μ€ν€λ§λ§ μ‘΄μ¬

λ°μ΄ν°λ² μ΄μ€ νμΌμ μ μ₯λλ λ°μ΄ν°μ νν

κ°μ²΄ κ°μ κ΄κ³ λ° λ¬΄κ²°μ± μ μ½ μ‘°κ±΄μ λν λͺμΈ μ μ

<aside>
π **λ¬΄κ²°μ± μ μ½ μ‘°κ±΄**
Β : λ°μ΄ν°λ² μ΄μ€μ μ νμ±, μΌκ΄μ±μ λ³΄μ₯νκΈ° μν΄ μ μ₯, μ­μ , μμ  λ±μ μ μ½νκΈ° μν μ‘°κ±΄

</aside>

<br><br>

**+Β λ΄λΆ μ€ν€λ§**

---

λ΄λΆ μ€ν€λ§ Internal Schema = μ μ₯ μ€ν€λ§ Storage Schema

λ¬Όλ¦¬μ μΈ μ μ₯μ₯μΉμ μμ₯μμ λ³Έ λ°μ΄ν°λ² μ΄μ€ κ΅¬μ‘°

κ°λ μ€ν€λ§λ₯Ό λμ€ν¬ κΈ°μ΅μ₯μΉμ λ¬Όλ¦¬μ μΌλ‘ κ΅¬ννκΈ° μν λ°©λ²μ κΈ°μ ν κ²

μ μ₯λ  λ°μ΄ν° ν­λͺ©μ λ΄λΆ λ μ½λ νμ, λ¬Όλ¦¬μ  μμ λ±μ λνλ

<br><br>

π©Β **μλΉ λ΅λ³**

---

Q. μ€ν€λ§κ° λ¬΄μμΈκ°μ.

μ€ν€λ§λ κ°μ²΄λ μμ±, κ΄κ³ λ± λ°μ΄ν°λ² μ΄μ€μ κ΅¬μ‘°μ μ μ½μ‘°κ±΄μ λν μ λ°μ μΈ λͺμΈλ₯Ό κΈ°μ ν λ©νλ°μ΄ν°μλλ€. μ€ν€λ§μ 3κ³μΈ΅μΌλ‘λ μΈλΆ μ€ν€λ§, κ°λ μ€ν€λ§, λ΄λΆ μ€ν€λ§κ° μμ΅λλ€.

μΈλΆ μ€ν€λ§λ μ¬μ©μμ μμ₯μμ λ°μ΄ν°λ² μ΄μ€μ λΌλ¦¬μ  κ΅¬μ‘°λ₯Ό μ μν κ²μ΄κ³ , κ°λ μ€ν€λ§λ λ¬Όλ¦¬μ μΈ κ΅¬νμ κ³ λ €νμ§ μμ λ°μ΄ν°λ² μ΄μ€μ μ μ²΄ μ‘°μ§μ λν λΌλ¦¬μ μΈ κ΅¬μ‘°μ΄λ©°, λ΄λΆ μ€ν€λ§λ λ¬Όλ¦¬μ μΈ μ μ₯μ₯μΉμ μμ₯μμ λ³Έ λ°μ΄ν°λ² μ΄μ€ κ΅¬μ‘°μλλ€.

<br><br>

π©Β **μ°Έκ³ **

---

λΈλ‘κ·Έ

[[DB λ°μ΄ν°λ² μ΄μ€] μ€ν€λ§(Schema)μ κ°λ λ° νΉμ§](https://iingang.github.io/posts/DB-schema/#%EC%99%B8%EB%B6%80-%EC%8A%A4%ED%82%A4%EB%A7%88-external-schema--%EC%82%AC%EC%9A%A9%EC%9E%90-%EB%B7%B0view)

[[DB] μ€ν€λ§(Schema)λ? μΈλΆμ€ν€λ§, κ°λμ€ν€λ§, λ΄λΆμ€ν€λ§](https://code-lab1.tistory.com/114)

<br><br>
