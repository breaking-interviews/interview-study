## **π 4-way Handshakeλβ**
β
TCP/IP λ€νΈμν¬ νκ²½μμ μλ²μ ν΄λΌμ΄μΈνΈμ μ°κ²°μ ν΄μ (μΈμ μ’λ£)νλλ° νμν νλ‘μΈμ€μ΄λ€.
β
### β TCP FLAG
β
| FLAG | μ€λͺ |
| --- | --- |
| SYN(μ°κ²° μμ²­ νλκ·Έ) | \- TCPμμ μΈμμ μ±λ¦½ν  λ κ°μ₯ λ¨Όμ  λ³΄λ΄λ ν¨ν·, μνμ€ λ²νΈλ₯Ό μμμ μΌλ‘ μ€μ νμ¬ μΈμμ μ°κ²°νλ λ°μ    μΈμμ μ°κ²°νλ λ°μ  μ¬μ©λλ©° μ΄κΈ°μ μνμ€ λ²νΈλ₯Ό λ³΄λ΄κ² λλ€. |
| ACK(μλ΅ νλκ·Έ) | \- μλλ°©μΌλ‘λΆν° ν¨ν·μ λ°μλ€λ κ²μ μλ €μ£Όλ ν¨ν·μ΄λ€.   \- λ€λ₯Έ νλκ·Έμ κ°μ΄ μΆλ ₯λλ κ²½μ°λ μλ€.   \- λ°λ μ¬λμ΄ λ³΄λΈ μ¬λ μνμ€ λ²νΈμ TCP κ³μΈ΅μμ κΈΈμ΄ λλ λ°μ΄ν° μμ λν κ²κ³Ό κ°μ ACKλ₯Ό λ³΄λΈλ€. (μΌλ°μ μΌλ‘ + 1 νμ¬ λ³΄λΈλ€)   \- ACK μλ΅μ ν΅ν΄ λ³΄λΈ ν¨ν·μ λν μ±κ³΅, μ€ν¨λ₯Ό νλ¨νμ¬ μ¬μ μ‘ νκ±°λ λ€μ ν¨ν·μ μ μ‘νλ€. |
| FIN(μ°κ²° μ’λ£ νλκ·Έ) | \- μΈμ μ°κ²°μ μ’λ£μν¬ λ μ¬μ©λλ©° λμ΄μ μ μ‘ν  λ°μ΄ν°κ° μμμ λνλΈλ€. |
| RST(μ°κ²° μ¬μ€μ  νλκ·Έ) | \-μ¬μ€μ (Reset)μ νλ κ³Όμ μ΄λ©° μλ°©ν₯μμ λμμ μΌμ΄λλ μ€λ¨ μμμ΄λ€.   \- λΉ μ μμ μΈ μΈμ μ°κ²° λκΈ°μ ν΄λΉνλ€.   \- μ΄ ν¨ν·μ λ³΄λ΄λ κ³³μ΄ νμ¬ μ μνκ³  μλ κ³³κ³Ό μ¦μ μ°κ²°μ λκ³ μ ν  λ μ¬μ©νλ€. |
| PSH(λ°μ΄λ£κΈ°) | \-TELNETκ³Ό κ°μ μνΈμμ©μ΄ μ€μν νλ‘ν μ½μ κ²½μ° λΉ λ₯Έ μλ΅μ΄ μ€μνλ°, μ΄ λ λ°μ λ°μ΄ν°λ₯Ό μ¦μ λͺ©μ μ§μΈ OSI 7 κ³μΈ΅μ Application κ³μΈ΅μΌλ‘ μ μ‘νλλ‘ νλ νλκ·Έμ΄λ€.   \- λνν νΈλν½μ μ¬μ©λλ κ²μΌλ‘ λ²νΌκ° μ±μμ§κΈ°λ₯Ό κΈ°λ€λ¦¬μ§ μκ³  λ°μ΄ν°λ₯Ό μ λ¬νλ€.   \- λ°μ΄ν°λ λ²νΌλ§ μμ΄ λ°λ‘ μ κ³μΈ΅μ΄ μλ 7κ³μΈ΅μ μμ©νλ‘κ·Έλ¨μΌλ‘ λ°λ‘ μ λ¬νλ€. |
| URG(κΈ΄κΈ λ°μ΄ν° νλκ·Έ) | \- Urgent pointer μ ν¨ν κ²μΈμ§λ₯Ό λνλΈλ€.   \- Urgent pointerλ μ μ‘νλ λ°μ΄ν° μ€μμ κΈ΄κΈν μ λ¬ν΄μΌ ν  λ΄μ©μ΄ μμ κ²½μ°μ μ¬μ©νλ€.   \- κΈ΄κΈν λ°μ΄ν°λ λ€λ₯Έ λ°μ΄ν°μ λΉν΄ μ°μ  μμκ° λμμΌ νλ€.   \- ex) ping λͺλ Ήμ΄ μ€ν λμ€ Ctrl + c μλ ₯ |
β
### β 4-way Handshake νλ‘μΈμ€
β
![image](https://user-images.githubusercontent.com/96826217/211199761-370de7d4-003e-4e40-9874-842c65a8613d.png)

β
1) ν΄λΌμ΄μΈνΈμμ μλ²μμ μ°κ²° μ’λ£λ₯Ό μν΄ μλ²μ **FIN** ν¨ν·μ λ³΄λ΄κ³  **FIN\_WAIT1** μνκ° λλ€.
β
(λ°λλ‘ μλ²μμ λ¨Όμ  λμ μ λ μλ€.)
β
2) μλ²λ ν΄λΌμ΄μΈνΈλ‘λΆν° **FIN**μ λ°κ³  μλ΅ ν¨ν· **ACK**μ λ³΄λΈλ€.
β
μνλ **CLOSE\_WAIT**κ° λλ€.
β
3) μλ²κ° ν΅μ μ΄ λλλ©΄, μ¦ μ°κ²°μ μ’λ£ν  μ€λΉκ° λλ©΄ ν΄λΌμ΄μΈνΈμκ² **FIN**ν¨ν·μ λ³΄λ΄κ³  **LAST\_WAIT** μνκ° λλ€.
β
4) ν΄λΌμ΄μΈνΈλ νμΈ ν¨ν· **ACK**μ λ³΄λ΄κ³  **TIME\_WAIT** μνκ° λλ€.
β
μ κ³Όμ μ ν΅ν΄ μλ²μ ν΄λΌμ΄μΈνΈλ μμ νκ² μΈμμ μ’λ£νκ² λλ€.

| μν | μ€λͺ |
| --- | --- |
| FIN\_WAIT1 | Closeλ₯Ό νΈμΆν μΈ‘μ μμΌμ΄ μ§μνλ μν, FINμ λ³΄λ |
| CLOST\_WAIT1 | Closeλ₯Ό λ°μΌλ©΄ CLOSE\_WAIT μνλ‘ μ§μνκ³  Ackλ₯Ό λ³΄λ |
| FIN\_WAIT2 | Ack μ νΈλ₯Ό λ°μ μμΌμ FIN\_WAIT1 -> FIN\_WAIT2λ‘ μνκ° λ³κ²½λλ€. |
| LAST\_WAIT | Close νΈμΆ ν μ§μνλ μν, FINμ λ³΄λ |
| TIME\_WAIT | Closeλ₯Ό λ°μΌλ©΄ μ§μνλ μν, ACKλ₯Ό λ³΄λ |
| CLOSE | μ°κ²° μ’λ£ |
