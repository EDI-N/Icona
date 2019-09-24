Changelog
=========



продолжение следует


python3.7 -mvirtualenv --no-site-packages --no-download /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest
/home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/python -m pip install --upgrade --cache-dir /home/docs/checkouts/readthedocs.org/user_builds/edi-n/.cache/pip pip
/home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/python -m pip install --upgrade --cache-dir /home/docs/checkouts/readthedocs.org/user_builds/edi-n/.cache/pip Pygments==2.3.1 setuptools==41.0.1 docutils==0.14 mock==1.0.1 pillow==5.4.1 alabaster>=0.7,<0.8,!=0.7.5 commonmark==0.8.1 recommonmark==0.5.0 sphinx<2 sphinx-rtd-theme<0.5 readthedocs-sphinx-ext<1.1
/home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/python -m pip install --exists-action=w --cache-dir /home/docs/checkouts/readthedocs.org/user_builds/edi-n/.cache/pip -r docs/requirements.txt
cat docs/conf.py
python /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/sphinx-build -T -E -b readthedocs -d _build/doctrees-readthedocs -D language=ru . _build/html
python /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/sphinx-build -T -b readthedocssinglehtmllocalmedia -d _build/doctrees-readthedocssinglehtmllocalmedia -D language=ru . _build/localmedia
python /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/sphinx-build -b latex -D language=ru -d _build/doctrees . _build/latex
cat latexmkrc 

I've been just working on with something similar and I found the solution here. What you need to do is to use a custom directive and add it to an existing writer. You can simply add the directive (with small modifications) from the link to the rst2html.py script and you are all set. See 

Примеры и рекомендации по использованию стилей управления формой, параметров макета и пользовательских компонентов для создания широкого спектра форм.
Обзор

Формы в Bootstrap по сути являются просто расширением наших Перезагруженных стилей форм с добавлением классов. Используйте эти классы для более точной настройки отображения и лучшей отрисовки на разных браузерах и устройствах.

Удостоверьтесь, что используете правильный атрибут type во всех формах ввода (т.е., email для почты и number для цифровой информации), это даст вам преимущества в виде новейших инструментов (таких как проверка email, выборка чисел и т.д.) контроля данных ввода.

Вот демонстрация стилей форм Bootstrap. Читайте документацию по требуемым классам, расположению форм и т.д.
Email address
We'll never share your email with anyone else.
Password
Check me out

<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

Инструменты контроля форм

Текстовые инструменты контроля – такие как <input>, <select> и <textarea> - стилизованы классом .form-control, который содержит основные стили внешнего вида, активного состояния, размерности и т.д.

Изучите наши обычные формы для дальнейшего понимания стилизации <select>.
Email address
Example select
Example multiple select
Example textarea

<form>
  <div class="form-group">
    <label for="exampleFormControlInput1">Email address</label>
    <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">
  </div>
  <div class="form-group">
    <label for="exampleFormControlSelect1">Example select</label>
    <select class="form-control" id="exampleFormControlSelect1">
      <option>1</option>
      <option>2</option>
      <option>3</option>
      <option>4</option>
      <option>5</option>
    </select>
  </div>
  <div class="form-group">
    <label for="exampleFormControlSelect2">Example multiple select</label>
    <select multiple class="form-control" id="exampleFormControlSelect2">
      <option>1</option>
      <option>2</option>
      <option>3</option>
      <option>4</option>
      <option>5</option>
    </select>
  </div>
  <div class="form-group">
    <label for="exampleFormControlTextarea1">Example textarea</label>
    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
  </div>
</form>

Для создания формы загрузки файлов замените .form-control на .form-control-file.
Example file input

<form>
  <div class="form-group">
    <label for="exampleFormControlFile1">Example file input</label>
    <input type="file" class="form-control-file" id="exampleFormControlFile1">
  </div>
</form>

Размерность

Для создания форм заданной высоты используются классы, такие как .form-control-lg и .form-control-sm.

<input class="form-control form-control-lg" type="text" placeholder=".form-control-lg">
<input class="form-control" type="text" placeholder="Default input">
<input class="form-control form-control-sm" type="text" placeholder=".form-control-sm">

<select class="form-control form-control-lg">
  <option>Large select</option>
</select>
<select class="form-control">
  <option>Default select</option>
</select>
<select class="form-control form-control-sm">
  <option>Small select</option>
</select>

«Только чтение»

Добавьте атрибут булеанова типа readonly в форму ввода для предотвращения возможности изменения значения ввода. Такие типы ввода выглядят светлее (как неактивные формы ввода), но сохраняют стандартный курсор.

<input class="form-control" type="text" placeholder="Readonly input here…" readonly>

Простой текст только для чтения

Если в ваших формах вы хотите стилизовать элементы <input readonly> как простой текст, используйте класс .form-control-plaintext для удаления оформления форм по умолчанию и сохранения правильных отступов.
Email
Password

<form>
  <div class="form-group row">
    <label for="staticEmail" class="col-sm-2 col-form-label">Email</label>
    <div class="col-sm-10">
      <input type="text" readonly class="form-control-plaintext" id="staticEmail" value="email@example.com">
    </div>
  </div>
  <div class="form-group row">
    <label for="inputPassword" class="col-sm-2 col-form-label">Password</label>
    <div class="col-sm-10">
      <input type="password" class="form-control" id="inputPassword" placeholder="Password">
    </div>
  </div>
</form>

Email
Password

<form class="form-inline">
  <div class="form-group mb-2">
    <label for="staticEmail2" class="sr-only">Email</label>
    <input type="text" readonly class="form-control-plaintext" id="staticEmail2" value="email@example.com">
  </div>
  <div class="form-group mx-sm-3 mb-2">
    <label for="inputPassword2" class="sr-only">Password</label>
    <input type="password" class="form-control" id="inputPassword2" placeholder="Password">
  </div>
  <button type="submit" class="btn btn-primary mb-2">Confirm identity</button>
</form>

Чекбоксы и кнопки «радио»

Чекбоксы и «радио», существовавшие по умолчанию, теперь модернизированы единым для обоих классом .form-check, цель которого – в улучшении их расположения и «поведения» их элементов HTML. Чекбоксы существуют для выбора одного или нескольких параметров из списка, а кнопки «радио» - одного.

Неактивные состояния чекбоксоы и "радио" поддерживаются, но для придания курсору функциональности not-allowed по наведению на родительский <label> вам потребуется добавить в .form-check-input атрибут disabled. Атрибут disabled будет применять более светлый цвет, чтобы указать состояние ввода.

Использование чекбоксов и "радио" имеет целью поддержать HTML-форму валидации и обеспечить понятные, доступные лейблы. Поэтому наши <input> и <label> - имеют одного родителя, в отличие от <input>, расположенного внутри <label>. Это немного более подробно, так как вы должны указывать атрибуты id и for для связи <input> и <label>.
По умолчанию (расположенные по вертикали)

По умолчанию, любое количество идущих один за другим чекбоксов и «радио» кнопок будет располагаться сверху вниз, а класс .form-check правильно отрегулирует пространство между ними.
Default checkbox
Disabled checkbox

<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
  <label class="form-check-label" for="defaultCheck1">
    Default checkbox
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheck2" disabled>
  <label class="form-check-label" for="defaultCheck2">
    Disabled checkbox
  </label>
</div>

Default radio
Second default radio
Disabled radio

<div class="form-check">
  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios1" value="option1" checked>
  <label class="form-check-label" for="exampleRadios1">
    Default radio
  </label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios2" value="option2">
  <label class="form-check-label" for="exampleRadios2">
    Second default radio
  </label>
</div>
<div class="form-check disabled">
  <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios3" value="option3" disabled>
  <label class="form-check-label" for="exampleRadios3">
    Disabled radio
  </label>
</div>

Встроенные

Группируйте чекбоксы или «радио» кнопки по одной горизонтальной линии, добавив класс .form-check-inline в любой элемент класса .form-check.
1
2
3 (disabled)

<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="inlineCheckbox1" value="option1">
  <label class="form-check-label" for="inlineCheckbox1">1</label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="inlineCheckbox2" value="option2">
  <label class="form-check-label" for="inlineCheckbox2">2</label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="inlineCheckbox3" value="option3" disabled>
  <label class="form-check-label" for="inlineCheckbox3">3 (disabled)</label>
</div>

1
2
3 (disabled)

<div class="form-check form-check-inline">
  <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="option1">
  <label class="form-check-label" for="inlineRadio1">1</label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="option2">
  <label class="form-check-label" for="inlineRadio2">2</label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio3" value="option3" disabled>
  <label class="form-check-label" for="inlineRadio3">3 (disabled)</label>
</div>

Без ярлыков

Добавьте класс .position-static в формы ввода, которые находятся внутри элемента класса .form-check и не имеют какого-либо пояснительного текста. Не забудьте добавить одну из форм «лейбла» для вспомогательных технологий (например, использовав aria-label).

<div class="form-check">
  <input class="form-check-input position-static" type="checkbox" id="blankCheckbox" value="option1" aria-label="...">
</div>
<div class="form-check">
  <input class="form-check-input position-static" type="radio" name="blankRadio" id="blankRadio1" value="option1" aria-label="...">
</div>

Расположение

Т.к. Bootstrap применяет display: block и width: 100% почти ко всем органам контроля форм, формы по умолчанию будут выстраиваться вертикально. Дополнительные классы можно использовать для создания вариаций расположения каждой отдельной формы.
Группы форм

Класс .form-group – самый простой путь придания формам некой структуры. Его единственная цель – создание вокруг надписи margin-bottom и включение контроля. В качестве приятного дополнения: поскольку это обычный класс, его можно использовать с <fieldset>, <div> или практически любым прочим элементом.
Example label
Another label

<form>
  <div class="form-group">
    <label for="formGroupExampleInput">Example label</label>
    <input type="text" class="form-control" id="formGroupExampleInput" placeholder="Example input">
  </div>
  <div class="form-group">
    <label for="formGroupExampleInput2">Another label</label>
    <input type="text" class="form-control" id="formGroupExampleInput2" placeholder="Another input">
  </div>
</form>

Сетка форм

Используйте их для расположения форм, которые требуют множественных колонок, различной ширины и других дополнительных параметров выравнивания.

<form>
  <div class="row">
    <div class="col">
      <input type="text" class="form-control" placeholder="Имя">
    </div>
    <div class="col">
      <input type="text" class="form-control" placeholder="Фамилия">
    </div>
  </div>
</form>

Ряд форм

Вы также можете заменить .row на класс .form-row, который есть разновидность нашего стандартного ряда сетки, который обладает возможностью «перебить» стандартно установленные расстояния между колонками и делает колонки более компактными.

<form>
  <div class="form-row">
    <div class="col">
      <input type="text" class="form-control" placeholder="Имя">
    </div>
    <div class="col">
      <input type="text" class="form-control" placeholder="Фамилия">
    </div>
  </div>
</form>

Более сложную разметку можно также создать системой сеток.
Email
Password
Address
Address 2
City
State
Zip
Check me out

<form>
  <div class="form-row">
    <div class="form-group col-md-6">
      <label for="inputEmail4">Email</label>
      <input type="email" class="form-control" id="inputEmail4" placeholder="Email">
    </div>
    <div class="form-group col-md-6">
      <label for="inputPassword4">Password</label>
      <input type="password" class="form-control" id="inputPassword4" placeholder="Password">
    </div>
  </div>
  <div class="form-group">
    <label for="inputAddress">Address</label>
    <input type="text" class="form-control" id="inputAddress" placeholder="1234 Main St">
  </div>
  <div class="form-group">
    <label for="inputAddress2">Address 2</label>
    <input type="text" class="form-control" id="inputAddress2" placeholder="Apartment, studio, or floor">
  </div>
  <div class="form-row">
    <div class="form-group col-md-6">
      <label for="inputCity">City</label>
      <input type="text" class="form-control" id="inputCity">
    </div>
    <div class="form-group col-md-4">
      <label for="inputState">State</label>
      <select id="inputState" class="form-control">
        <option selected>Choose...</option>
        <option>...</option>
      </select>
    </div>
    <div class="form-group col-md-2">
      <label for="inputZip">Zip</label>
      <input type="text" class="form-control" id="inputZip">
    </div>
  </div>
  <div class="form-group">
    <div class="form-check">
      <label class="form-check-label">
        <input class="form-check-input" type="checkbox"> Check me out
      </label>
    </div>
  </div>
  <button type="submit" class="btn btn-primary">Sign in</button>
</form>

Горизонтальные формы

Создайте горизонтальные формы с помощью сеток, добавив класс .row к группам форм и используя классы .col-*-* для задания ширины ваших надписей и элементов контроля. Обязательно добавьте класс .col-form-label также и в ваши <label> для того, чтобы они приобрели вертикальное центрирование относительно связанных с ними элементов контроля форм.

Временами вам может понадобиться классы марджина или паддинга, чтобы создать классное выравнивание. Например, мы удалили padding-top в наших вертикально расположенных лейблах ввода "радио", для лучшего выравнивания текста.
Email
Password
Radios
First radio
Second radio
Third disabled radio
Checkbox
Example checkbox

<form>
  <div class="form-group row">
    <label for="inputEmail3" class="col-sm-2 col-form-label">Email</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="inputEmail3" placeholder="Email">
    </div>
  </div>
  <div class="form-group row">
    <label for="inputPassword3" class="col-sm-2 col-form-label">Password</label>
    <div class="col-sm-10">
      <input type="password" class="form-control" id="inputPassword3" placeholder="Password">
    </div>
  </div>
  <fieldset class="form-group">
    <div class="row">
      <legend class="col-form-label col-sm-2 pt-0">Radios</legend>
      <div class="col-sm-10">
        <div class="form-check">
          <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios1" value="option1" checked>
          <label class="form-check-label" for="gridRadios1">
            First radio
          </label>
        </div>
        <div class="form-check">
          <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios2" value="option2">
          <label class="form-check-label" for="gridRadios2">
            Second radio
          </label>
        </div>
        <div class="form-check disabled">
          <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios3" value="option3" disabled>
          <label class="form-check-label" for="gridRadios3">
            Third disabled radio
          </label>
        </div>
      </div>
    </div>
  </fieldset>
  <div class="form-group row">
    <div class="col-sm-2">Checkbox</div>
    <div class="col-sm-10">
      <div class="form-check">
        <input class="form-check-input" type="checkbox" id="gridCheck1">
        <label class="form-check-label" for="gridCheck1">
          Example checkbox
        </label>
      </div>
    </div>
  </div>
  <div class="form-group row">
    <div class="col-sm-10">
      <button type="submit" class="btn btn-primary">Sign in</button>
    </div>
  </div>
</form>

Размеры надписей горизонтальных форм

Обязательно используйте классы .col-form-label-sm или .col-form-label-lg в своих <label> для того, чтобы размеры шрифтов названия формы и вспомогательной надписи в пустой форме (т.н. placeholder) ввода совпадали.


.. container:: test
    :name: abrakadabra

    супер текст на который идет ссылка.... или нет

Альо!!!!!
