Для транслитерации кириллицы в латиницу нужно два (~~или три~~) алфавита на латинице. Первый с диакритическими знаками для записи там, где можно их использовать. Например имён спортсменов и политиков в СМИ, географических названий и так далее. Второй для случаев если нельзя использовать первый. Который состоит только из букв основной латиницы (ASCII) и апострофа там, где это допустимо. Например для записи имён в банковских система, URL-ссылки, адреса электронной почты.  
Пример первого: «**Р 8.2**», второго: «**Р 2 ASCII 2б**».

?Третий «ASCII 6а» можно использовать если есть только клавиатура с основной латиницей.  
<details>
  <summary>Сравнении с кириллицей</summary>

**Р 8.2**  
В тексте приблизительно на 1% больше букв, а объём в байта меньше на 45% в сравнении с кириллицей.
	
**ASCII 6а**  
В тексте приблизительно на 6% больше букв, а объём в байта меньше на 46% в сравнении с кириллицей.

**Р 2 ASCII 2в**  
В тексте приблизительно на 8% больше букв, а объём в байта меньше на 46% в сравнении с кириллицей.
	
</details>

Каждый из вариантов можно назвать как:
* Первый - Основной
* Второй - Общий
* Третьи - Локальный

В первый и второй можно добавить правило ъ[оуаыиэ] -> апостроф[оуаыиэ]. Если использовать [апостроф](https://en.wikipedia.org/wiki/Apostrophe#Unicode), то только как разделитель перед не йотированными гласными. А если вместо **ь**, то из-за большей частотность чем **ъ** слова и текст будут хуже восприниматься. Хотя в некоторых вариантах в которых используется одна и таже буква для **й** и **ь** он так же ставиться между **ьо**: **Р 7** - "počtalj'on"; **ASCII 6а** - "poctalj'on"; **Р 2 ASCII 2в** - "pochtali'on".

Какой апостроф выбрать[?](https://tedclancy.wordpress.com/2015/06/03/which-unicode-character-should-represent-the-english-apostrophe-and-why-the-unicode-committee-is-very-wrong/)  
Для первого: `U+02BC` или `U+2019` или `U+0027`  
Для второго: `U+0027`. Здесь нет выбора, только ASCII.

Второй вариант должен быть сделан на основе требований к именам на [банковских картах](https://stackoverflow.com/questions/2004532/credit-card-validation-can-card-name-contain-non-ascii-characters).  
Буква **щ** - **sch** / **shch**. Намример для имён **sch**, а для URL-ссылылок **shch**.  
«**Р 2 ASCII 2в**» плюс этого варианта то, что есть мягкий знак, ~~а минус буква "**w**". Ещё есть буквы **j**, **q** и **x** которые трудно применить в этом варианте.~~ и не нужен третий.

Аббревиатуры:
Кириллица | Р 8 | Р 2 ASCII 2 | ASCII 6
 :---: | :---: | :---: | :---:
БЭВЕЦХ | BEVJECH | BEVYECKH | BEVJEQCH

Варианты без апострофа:  
1. Р 8  
2. Р 2 ASCII 2  
3. ASCII 6

<details>
  <summary>?</summary>
  
Для любого вида латиницы самые спорны вопросы:
- что использовать для буквы "**й**"
- что использовать для буквы "**х**"
- что использовать для буквы "**щ**"
- что использовать для буквы "**ы**"
- что использовать для буквы "**ь**"
- если используются йотированные гласные, то они  не пишутся в начале слова
- использовать или нет мягкие согласные
- после букв "**ж ч ш щ**" не пишутся "**ь ё ю я**"
- нужно ли использовать апостроф (для **ь** или **ъ**)
  
</details>

Примеры раскладок клавиатуры:  
[SCUKE4 (ЩЦУКЕ4)](https://raw.githubusercontent.com/2k1dmg/c2l/main/files/RuSCUKE4.klc) «**Р 8**»

```
ħ c u k e n g š j z h ě
 f y v a p r o l d ž ō
  ā č s m i t ì b ū
```

<details>
  <summary>другие</summary>
  
[SCUKEN (ЩЦУКЕН)](https://raw.githubusercontent.com/2k1dmg/c2l/main/files/RuSCUKEN.klc) «**Р 2в**»

```
ŝ c u k e n g š y z x ê
 f î v a p r o l d ž ō
  ā č s m i t j b ū
```
 
[SCUKE2 (ЩЦУКЕ2)](https://raw.githubusercontent.com/2k1dmg/c2l/main/files/RuSCUKE2.klc) «**Р 2ва/б**»

```
ŝ c u k e n g š y z h ê
 f î v a p r o l d ž ō
  ā č s m i t j b ū
```

[SCUKE3 (ЩЦУКЕ3)](https://raw.githubusercontent.com/2k1dmg/c2l/main/files/RuSCUKE3.klc) «**Р 2ва/ба**»

```
  ź ŕ ď ś ń ľ ť
ŝ c u k e n g š y z h ê
 f î v a p r o l d ž ō
  ā č s m i t j b ū
```

[ECUKEN (ЭЦУКЕН)](https://raw.githubusercontent.com/2k1dmg/c2l/main/files/RuECUKEN.klc) «**Р 2б**»

```
ê c u k e n g š y z h
 f î v a p r o l d ž ō
  ā č s m i t j b ū
```
  
</details>

?**Ō ō** -> **Ë ë**, **Ē ē**

<table>
   <tbody>
      <tr>
         <th colspan="34">Алфавит</th>
      </tr>
      <tr align=center>
         <th>Кириллица</th>
         <td>А</td>
         <td>Б</td>
         <td>В</td>
         <td>Г</td>
         <td>Д</td>
         <td>Е</td>
         <td>Ё</td>
         <td>Ж</td>
         <td>З</td>
         <td>И</td>
         <td>Й</td>
         <td>К</td>
         <td>Л</td>
         <td>М</td>
         <td>Н</td>
         <td>О</td>
         <td>П</td>
         <td>Р</td>
         <td>С</td>
         <td>Т</td>
         <td>У</td>
         <td>Ф</td>
         <td>Х</td>
         <td>Ц</td>
         <td>Ч</td>
         <td>Ш</td>
         <td>Щ</td>
         <td>Ъ</td>
         <td>Ы</td>
         <td>Ь</td>
         <td>Э</td>
         <td>Ю</td>
         <td>Я</td>
      </tr>
      <tr align=center>
         <th>Р 8.2</th>
         <td>A</td>
         <td>B</td>
         <td>V</td>
         <td>G</td>
         <td>D</td>
         <td>JE/E</td>
         <td>JO/Ō</td>
         <td>Ž</td>
         <td>Z</td>
         <td>I</td>
         <td>J</td>
         <td>K</td>
         <td>L</td>
         <td>M</td>
         <td>N</td>
         <td>O</td>
         <td>P</td>
         <td>R</td>
         <td>S</td>
         <td>T</td>
         <td>U</td>
         <td>F</td>
         <td>H/CH</td>
         <td>C</td>
         <td>Č</td>
         <td>Š</td>
         <td>Ħ</td>
         <td>-</td>
         <td>Y</td>
         <td>Ì</td>
         <td>E/Ě</td>
         <td>JU/Ū</td>
         <td>JA/Ā</td>
      </tr>
      <tr align=center>
         <th>Р 2 ASCII 2б</th>
         <td>A</td>
         <td>B</td>
         <td>V</td>
         <td>G</td>
         <td>D</td>
         <td>YE/E</td>
         <td>YO/IO</td>
         <td>ZH</td>
         <td>Z</td>
         <td>I</td>
         <td>Y</td>
         <td>K</td>
         <td>L</td>
         <td>M</td>
         <td>N</td>
         <td>O</td>
         <td>P</td>
         <td>R</td>
         <td>S</td>
         <td>T</td>
         <td>U</td>
         <td>F</td>
         <td>KH</td>
         <td>C</td>
         <td>CH</td>
         <td>SH</td>
         <td>SCH</td>
         <td>-</td>
         <td>Y</td>
         <td>-</td>
         <td>E</td>
         <td>YU/IU</td>
         <td>YA/IA</td>
      </tr>
      <tr align=center>
         <th>ASCII 6а</th>
         <td>A</td>
         <td>B</td>
         <td>V</td>
         <td>G</td>
         <td>D</td>
         <td>JE/E/IE</td>
         <td>JO/OH/IO</td>
         <td>GZ</td>
         <td>Z</td>
         <td>I</td>
         <td>J</td>
         <td>K</td>
         <td>L</td>
         <td>M</td>
         <td>N</td>
         <td>O</td>
         <td>P</td>
         <td>R</td>
         <td>S</td>
         <td>T</td>
         <td>U</td>
         <td>F</td>
         <td>CH</td>
         <td>Q</td>
         <td>C</td>
         <td>X</td>
         <td>XC</td>
         <td>-</td>
         <td>Y</td>
         <td>J</td>
         <td>E/WE</td>
         <td>JU/UH/IU</td>
         <td>JA/AH/IA</td>
      </tr>
      <tr align=center>
         <th>Р 2 ASCII 2в</th>
         <td>A</td>
         <td>B</td>
         <td>V</td>
         <td>G</td>
         <td>D</td>
         <td>YE/E</td>
         <td>YO/IO</td>
         <td>ZH</td>
         <td>Z</td>
         <td>I</td>
         <td>Y</td>
         <td>K</td>
         <td>L</td>
         <td>M</td>
         <td>N</td>
         <td>O</td>
         <td>P</td>
         <td>R</td>
         <td>S</td>
         <td>T</td>
         <td>U</td>
         <td>F</td>
         <td>H/KH</td>
         <td>C/TZ</td>
         <td>CH</td>
         <td>SH</td>
         <td>SC</td>
         <td>-</td>
         <td>Y/W</td>
         <td>I/E</td>
         <td>E/WE</td>
         <td>YU/IU</td>
         <td>YA/IA</td>
      </tr>
   <tbody>
<table>

![ASCII 6](files/ascii6.png?raw=true "ASCII 6 / Шрифт: Learning Curve BV")
*ASCII 6*
 
 <details>
  <summary>Приблизительная частотность букв Р 8</summary>

``` 
Буква	Ранг	%
o	1	10.726
a	2	9.168
e	3	8.281
n	4	6.482
t	5	6.422
i	6	6.203
s	7	5.109
l	8	4.487
v	9	4.194
r	10	4.117
k	11	3.651
m	12	3.478
d	13	2.927
p	14	2.895
u	15	2.844
ì	16	2.146
j	17	2.009
ā	18	1.751
č	19	1.712
y	20	1.619
b	21	1.568
z	22	1.539
g	23	1.476
ž	24	1.009
š	25	0.984
h	26	0.800
ō	27	0.648
c	28	0.611
ū	29	0.605
ħ	30	0.353
f	31	0.169
ě	32	0.015
		(306212)
```

</details>
 
[userscript](https://greasyfork.org/scripts/21717)
