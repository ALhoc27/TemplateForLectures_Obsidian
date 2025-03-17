<table class="language-java_td" style="width: 99%; border-collapse: collapse; margin-bottom: 5px;">
	<tr>
		<strong style="font-size: 1.1em; color: #333; color: #1E587F;">Пример таблицы с двумя большими блоками кода:</strong>
    </tr>
    <tr>
        <td style="padding: 5px 10px; border: 1px solid #ddd; background-color: #f2efed">
            <strong style="font-size: 1em; color: #333; line-height: 1.7;"><span style="border: 1px solid black; padding: 2px;">#1</span>
		&nbsp; Сравнение без <code>Objects.equals()</code></strong> <!-- Заголовок первой колонки-->
			<br/>
Если вы используете стандартный метод <code>equals()</code>, необходимо учитывать ситуацию с <code>null</code> вручную:
			<br/>
        </td>
        <td style="padding: 5px 10px; border: 1px solid #ddd; background-color: #f2efed">
            <strong style="font-size: 1em; color: #333; line-height: 1.7;"><span style="border: 1px solid black; padding: 2px;">#2</span>
		&nbsp; Сравнение с <code>Objects.equals()</code></strong>  <!-- Заголовок второй колонки-->
		<br/>
С <code>Objects.equals()</code> код становится проще и безопаснее:
        </td>
    </tr>
    <tr>
        <td style="padding: 5px 10px; border: 1px solid #ddd;">
            <pre class="language-java_td" style="background-color: #f4f4f4; color: #f8f8f8; margin: 0px; padding: 0px 10px; border-radius: 5px; font-size: 0.9em; overflow-x: auto;">
				<code class="language-java language-java_td" style="font-family: 'Courier New', monospace; padding: 0px; margin: 0px;">
String str1 = null;
String str2 = "Java";
 
// Проверка вручную
if (str1 != null && str1.equals(str2)) {  🔴
    System.out.println("Равны");
} else {
    System.out.println("Не равны");
}
				</code>
            </pre>
        </td>
        <td style="padding: 5px 10px; border: 1px solid #ddd;">
            <pre style="background-color: #f4f4f4; color: #f8f8f8; margin: 0px; padding: 0px 10px; border-radius: 5px; font-size: 0.9em; overflow-x: auto;">
				<code class="language-java language-java_td" style="font-family: 'Courier New', monospace; padding: 0px; margin: 0px;">
String str1 = null;
String str2 = "Java";
 
if (Objects.equals(str1, str2)) {
🔴  System.out.println("Равны");
} else {
    System.out.println("Не равны");
}
				</code>
            </pre>
        </td>
    </tr>
    <tr>
	    <td>
	    Краткое пояснение:
	    </td>
	    <td>
	    Краткое пояснение:
	    </td>
    </tr>
</table>

###### Подробнее <span style="border: 1px solid black; padding: 2px; line-height: 1.75;">#1</span>: &nbsp; <br/>

###### Подробнее <span style="border: 1px solid black; padding: 2px; line-height: 1.75;">#2</span>: &nbsp; <br/>



> - **Замени все <> на ＜＞**
> - **Поставь в коде пробелы где пустая строка**
> - 🔴 🔵 🟠 ⚫️ 🟤 🟣 **шарик 2 пробела**