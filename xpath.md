## Задачи по XPath

### xpath.1

Входные данные:

    <persons>
        <person>
            <login>robot</login>
            <email>robot@somehost.ru</email>
            <phone type="mobile">223-322-223-322</phone>
            <group>xslt</group>
        </person>
        <person>
            <login>human</login>
            <email>human@somehost.ru</email>
            <phone type="work">666</phone>
            <phone type="mobile">123-456-321-654</phone>
            <group>xslt</group>
        </person>
        <person>
            <login>kiborg</login>
            <email>kiborg@somehost.ru</email>
            <group>html</group>
        </person>
        <person>
            <login>botanidze</login>
            <email>sergey@somehost.ru</email>
            <phone type="work">03</phone>
            <group>html</group>
        </person>
    </persons>

*   Выбрать людей, у которых есть телефон.
*   Выбрать людей, у которых есть мобильный телефон.
*   Выбрать людей, у которых есть и рабочий, и мобильный телефон.
*   Выбрать людей, у которых email начинается с `login@`.
*   Выбрать людей, принадлежащих к группе html.
*   Выбрать людей, у которых "длинный" логин (длиннее трех символов).
*   Выбрать для каждого человека по одному его контакту -
    мобильный телефон, рабочий телефон или email (что-нибудь одно, все равно что).
*   Выбрать для каждого контакта его рабочий телефон, если нет рабочего, то мобильный,
    если нет никакого телефона, то email.

---

### xpath.2

Входные данные:

    <items>
        <item id="1" class="a">
            <item id="1.1" class="b">
                <item id="1.1.1" class="a">
                    <item id="1.1.1.1" class="a">3</item>
                    <item id="1.1.1.2" class="b">7</item>
                    <item id="1.1.1.3" class="a">2</item>
                </item>
            </item>
            <item id="1.2" class="a">9</item>
        </item>
        <item id="2" class="b">
            <item id="2.1" class="a">
                <item id="2.1.1" class="b">4</item>
                <item id="2.1.2" class="a">8</item>
            </item>
            <item id="2.2" class="c">9</item>
            <item id="2.3" class="a">
                <item id="2.3.1" class="b">2</item>
            </item>
        </item>
        <item id="3" class="b">
            <itemd id="3.1" class="c">3</item>
        </item>
    </items>

*   Выбрать все ноды, "глубина залегания" которых является четным числом
    (для корневого элемента "глубина" равно 0.
*   Выбрать все ноды, у которых есть "старший брат" и "младший брат".
*   Выбрать все ноды, у "деда" которых ровно 6 потомков.
*   Выбрать все ноды, у которых есть предок и потомок с одинаковым классом.
*   Вычислить максимальное и минимальное значение среди всех `item`'ов.

---

### xpath.3

Входные данные:

    <items>
        <good>1,3,4</good>
        <bad>2,3,5</bad>
        <item id="first">
            <value>50</value>
            <related>
                <id>second</id>
                <id>third</id>
                <id>fourth</id>
            </related>
        </item>
        <item id="second">
            <value>20</value>
            <related>
                <id>first</id>
            </related>
        </item>
        <item id="third">
            <value>30</value>
            <related>
                <id>fourth</id>
            </related>
        </item>
        <item id="fourth">
            <value>10</value>
            <related>
                <id>first</id>
            </related>
        </item>
        <item id="last">
            <value>40</value>
            <related>
                <id>first</id>
            </related>
        </item>
    </items>

*   Выбрать `item`'ы, у которых `value` совпадает
    с порядковым номером в списке, умноженным на 10.
*   Выбрать `item`'ы, у которых `value` больше, чем у
    следующего за ним `item`'а.
*   Выбрать все "хорошие" ноды.
*   Выбрать ноды, являющиеся и "хорошими", и "плохими".
*   Выбрать все ноды, не связанные с "плохими" нодами.

