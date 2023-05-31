<h1>Втора лабораториска вежба по Софтверско инженерство</h1>

<h2>Бојана Драгановска 183199</h2>

<h3>Control Flow Graph</h3>


![cfg drawio](https://github.com/Bojana-Draganovska/SI_2023_lab2_183199/assets/96067158/0a319a5f-8e4f-437f-bfe1-0adc2eff302d)

<h3>Цикломатска комплексност</h3>

<p>Цикломатската комплексност на графот е 8. Резултатот се добива по број на региони, односно колку независни патеки имаме во графот.</p>

<h3>Тест случаи според критериумот Every branch</h3>

<ul>
  <li>1 - 2</li>
  <li>2 - 3</li>
  <li>2 - 4</li>
  <li>3 - 37</li>
  <li>4 - 5</li>
  <li>5 - 6</li>
  <li>5 - 7</li>
  <li>7 - 8</li>
  <li>8 - 9</li>
  <li>9 - 10</li>
  <li>9 - 20</li>
  <li>10 - 11.1</li>
  <li>11.1 - 11.2</li>
  <li>11.2 - 12</li>
  <li>11.2 - 19</li>
  <li>12 - 13</li>
  <li>13 - 14</li>
  <li>13 - 15</li>
  <li>15 - 16</li>
  <li>16 - 17</li>
  <li>16 - 18</li>
  <li>18 - 19</li>
  <li>19 - 11.3</li>
  <li>19 - 20</li>
  <li>20 - 21</li>
  <li>21 - 22</li>
  <li>22 - 23</li>
  <li>23 - 24</li>
  <li>24 - 25</li>
  <li>24 - 26</li>
  <li>26 - 36</li>
  <li>26 - 27</li>
  <li>27 - 28</li>
  <li>28 - 29.1</li>
  <li>28 - 35</li>
  <li>29.2 - 30</li>
  <li>29.2 - 34</li>
  <li>30 - 31</li>
  <li>30 - 32</li>
  <li>32 - 33</li>
  <li>33 - 29.3</li>
  <li>34 - 35</li>
  <li>35 - 36</li>
  <li>36 - 37</li>
</ul>
  
  <p>@Test</p>
  <p>void everyBranchTest() {</p>
  <p>RuntimeException ex;</p>
  <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(null, null, null));</p>
  <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
  <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function("User", null, null));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
   <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(123, "123", null));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
   <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(123, 2, "user@example.com"));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
    <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(123, 2, "user"));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
  <p>}</p>
  
  <h3>Тест случаи според критериумот Multiple Condition</h3>
  
   <p>@Test</p>
  <p>void multipleConditionTest() {</p>
   <p>RuntimeException ex;</p>
   <p>// if (user==null || user.getPassword()==null || user.getEmail()==null)</p>
   <p>// TXX</p>
   <p>// FTX</p>
   <p>// FFT</p>
   <p>// FFF</p>
   <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function("User", null, null));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
   <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(123, "123", null));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
   <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(123, 2, "user@example.com"));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
    <p>ex = assertThrows(RuntimeException.class, () -> SILab2.function(123, 2, "user"));</p>
   <p>assertTrue(ex.getMessage().contains("Mandatory information missing!"));</p>
   <p>}</p>

<h3>Објаснување на напишаните unit тестови</h3>
<p>Unit тестовите се напишани за да се исполнат сите услови и да можат да се поминат сите exceptions, во нашиов случај имаме еден exception. Со употреба на assertThrows се фаќаат exceptions кои се праќаат во „ex“, a за да може да се провери дали се фрлил соодветниот exception се користи assertTrue за дадениот влез. 

Со multiple condition се проверува дадениот if услов. Исто така и овде се користи assertThrows и assertTrue за фаќање и проверување дали е точен даден exception.</p>
