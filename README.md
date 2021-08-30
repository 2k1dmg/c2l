Для транслитерации кириллицы в латиницу нужно два (~~или три~~) алфавита на латинице. Первый с диакритическими знаками для записи там, где можно их использовать. Например имён спортсменов и политиков в СМИ, географических названий и так далее. Второй для случаев если нельзя использовать первый. Который состоит только из букв основной латиницы (ASCII) и апострофа там, где это допустимо. Например для записи имён в банковских система, URL-ссылки, адреса электронной почты.  
Пример первого: «**Р 8.2+**», второго: «**Р 2 ASCII 2в+**» (буква "ё" в которых обязательна).

?Третий «**Р 2 ASCII 2в+**» можно использовать если есть только клавиатура с основной латиницей (требования к букве "**ё**" такие же как и в кириллице и можно писать "ь ё ю я" после "ж ч ш щ"). У "ASCII 6а" специфические правила хотя и меньше диграфов.

?Четвёртый «**Т 5**» зеркальный кириллице и может применяться как "Научный".

Можно добавить (кроме варинтов "**Т**"), что после букв "ж ч ш щ" не пишутся "ь ё ю я" ("ё ю я" - "о у а").

<details> 
  <summary>Описаные разных видов латинизации:</summary>

- ASCII - любые буквы из ASCII
- Т - одна буква кириллицы равна одной букве латиницы
- Р - романизация
- Р ASCII - латинизация по правилам английского языка
	
</details>

Такие правила и выбор букв основан на том, что те кто будут читать:
1. В основной своей массе не владеют русским языком.
2. Общий для всех.
3. Знают русский язык, но под рукой нет клавиатуры с кириллицей.

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
«**Р 2 ASCII 2в**» с **ё** - Общий  
«**Р 2 ASCII 2г**» без **ё** - Локальный

Аббревиатуры:
Кириллица | Р 8 | Р 2 ASCII 2 | ASCII 6
 :---: | :---: | :---: | :---:
БЭВЕЦХ | BEVJECH | BEVYECKH | BEVJEQCH

Варианты без апострофа:  
1. Р 8  
2. Р 2 ASCII 2  
3. ASCII 6

#### Спорные вопросы
<details>
  <summary>?</summary>
  
Для любого вида латиницы самые спорные вопросы:
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

#### Ответы
<details>
  <summary>«Р 8.2+»</summary>
  
- для "й" в большинстве европейских и славянских языков используется "j"
- "х" в начале слов и после гласных кроме "и" - "h" в остальных случаях "ch". Так лучше смотрится "их" - "ich" / "ih" 
- для "щ" - "ħ" лучше различается в тексте по сравнению с "ś ŝ"
- для "ы" в большинстве славянских языков используется "y"
- для "ь" используется "ì" потому что лучше подходит для имён. Например "Darìā Natalìā". И лучше смотрится в конце слов в сравшнении с "î" očenì / očenî. Или другие производные буквы "i" например "î".
- йотированные гласные не пишутся в начале слов, а после твёрдого знака заменяют "ъе ъё ъю ъя" на "je jo ju ja"
- мягкие согласные не используют из-за малой их частотности и увеличения алфавита. Лучше использовать йотированные гласные "e ō ū ā" и мягкий знак "ì"
- после букв "ж ч ш щ" не пишутся "ь ё ю я". Легче читать
- для "ъ" используется "ĵ", а с физической клавиатуры набирается через AltGr + J или Ì. Хоть и частотность этого случая практически равна нулю лучше обойтись без апострофа который разделяет слово и ухудшает чтение. А апостроф оставить для ASCII варианта.

? **ё ю я** после согласных **io iu ia**  
? **ый** в конце слов **iuy**
</details>

?**Ō ō** -> **Ë ë**, **Ē ē**

#### Сопоставление букв кириллицы и латиниц
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
         <td>Ĵ</td>
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
         <td>SHCH</td>
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
         <td>XH</td>
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
         <td>C</td>
         <td>CH</td>
         <td>SH</td>
         <td>SHH</td>
         <td>-</td>
         <td>Y</td>
         <td>I/E</td>
         <td>E/EU</td>
         <td>YU/IU</td>
         <td>YA/IA</td>
      </tr>
      <tr align=center>
         <th>Р 2га</th>
         <td>A</td>
         <td>B</td>
         <td>V</td>
         <td>G</td>
         <td>D</td>
         <td>YE/E</td>
         <td>YO/Ŏ</td>
         <td>Ż</td>
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
         <td>X</td>
         <td>C</td>
         <td>Ç</td>
         <td>Ş</td>
         <td>Ħ</td>
         <td>-</td>
         <td>Ȳ</td>
         <td>Ì</td>
         <td>E/Ê</td>
         <td>YU/Ŭ</td>
         <td>YA/Ă</td>
      </tr>
      <tr align=center>
         <th>Т 5</th>
         <td>A</td>
         <td>B</td>
         <td>V</td>
         <td>G</td>
         <td>D</td>
         <td>E</td>
         <td>Ë</td>
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
         <td>H</td>
         <td>C</td>
         <td>Č</td>
         <td>Š</td>
         <td>Ħ</td>
         <td>Ĵ</td>
         <td>Y</td>
         <td>Ì</td>
         <td>Ě</td>
         <td>Ū</td>
         <td>Ā</td>
      </tr>
   <tbody>
<table>

### Латиница как основа
«**Р 8.3**»  
Всего 31 буква (плюс очень редкая **ĵ**).  
В определённых случаях буквы **х** и **щ** пишутся как дифтонги **ch** и **šì**.

### Тест

```javascript
'Р 8.2+ (жчшщь-ёюяь)': function(text) {
	return text
	.replace(/^([еёюяэ])/g, (found,p1) => ['je','jo','ju','ja','e']['еёюяэ'.indexOf(p1)])
	.replace(/ъ([еёюя])/g, (found,p1) => ['je','jo','ju','ja']['еёюя'.indexOf(p1)])
	.replace(/([бвгджзклмнпрстфхцчшщийь])х/g, '$1ch')
	// после букв "ж ч ш щ" не пишутся "ь ё ю я". Можно закомментировать эту строку
	.replace(/([жчшщ])(ь)?([иеёюя])?/g, (found,p1,p2,p3) => p1+(p2=='ь'&&p3?'j':'')+(p3?'ieoua'['иеёюя'.indexOf(p3)]:''))
	.replace(/[а-яё]/g, (found) => ['a','b','v','g','d','e','ō','ž','z','i','j','k','l','m','n','o','p','r','s','t','u','f','h','c','č','š','ħ','ĵ','y','ì','ě','ū','ā']['абвгдеёжзийклмнопрстуфхцчшщъыьэюя'.indexOf(found)]);
	//\u0027
}
```

### Разное
	
#### Частотность
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

Примеры раскладок клавиатуры:  
[SCUKE4 (ЩЦУКЕ4)](https://raw.githubusercontent.com/2k1dmg/c2l/main/files/RuSCUKE4.klc) «**Р 8**»

```
ħ c u k e n g š j z h ě
 f y v a p r o l d ž ō
  ā č s m i t ì b ū
```

OCUKEN «**Р 8.3**»
```
ō c u k e n g š j z h 
 f y v a p r o l d ž ě
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
	
#### Раскладка клавиатуры
[Русская (машинопись)](https://ru.wikipedia.org/wiki/%D0%99%D0%A6%D0%A3%D0%9A%D0%95%D0%9D#%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B0%D1%8F_(%D0%BC%D0%B0%D1%88%D0%B8%D0%BD%D0%BE%D0%BF%D0%B8%D1%81%D1%8C))

<details>
  <summary>Раскладки на основе Русская (машинопись)</summary>

**Татарская**
```
| № - / " : , . _ ? % ! ;
 й ө у к е н г ш ә з х ү
  ф ы в а п р о л д ң э
   я ч с м и т җ б ю һ
```

</details>
 
[userscript](https://greasyfork.org/scripts/21717)
