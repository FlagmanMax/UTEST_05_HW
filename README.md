# UTEST_05_HW
UTEST_05_HW

//5.1.
    //  Задание 1. Представьте, что вы работаете над разработкой простого приложения для записной книжки,
    //  которое позволяет пользователям добавлять, редактировать и удалять контакты.
    //  Ваша задача - придумать как можно больше различных тестов (юнит-тесты, интеграционные тесты,
    //  сквозные тесты) для этого приложения. Напишите название каждого теста, его тип и краткое описание того,
    //  что этот тест проверяет.

    @Test
    void testAddContact(){
        // unit-test
        // Add contact "Contact1"
        // Check that it is added with text "Contact1"
    }

    @Test
    void testAddContactWithTheSameName(){
         // unit-test
         // Add contact "Contact1"
         // Add another contact "Contact1"
         // Check that there still only 1 contact with name "Contact1"
    }

    @Test
    void testAddContactWithProhibitedName(){
         // unit-test
         // Add contact with prohibited name
         // Check that contact is not added
    }

    @Test
    void testAddContactInGui(){
          // E2E-test
          // Add contact via GUI
          // Check that contact is shown in list of contacts in GUI
    }

    @Test
    void testEditContact(){
         // integration-test
         // Add contact "Contact1"
         // Edit it to text "Contact2"
         // Check text "Contact2"
    }

    @Test
    void testEditContactWithTheSameData(){
         // integration-test
         // Add contact "Contact1"
         // Edit it to text "Contact1"
         // Check that there still only 1 contact with name "Contact1"
    }

    @Test
    void testEditContactViaGui(){
         // E2E-test
         // Add contact "Contact1" via GUI
         // Edit it to text "Contact2" via GUI
         // Check text "Contact2" via GUI
    }

    @Test
    void testDeleteContact(){
         // integration-test
         // Add contact "Contact1"
         // Delete contact "Contact1",
         // Check that there is no contact with text "Contact1"
    }

    @Test
    void testDeleteNotExistingContact(){
         // integration-test
         // Add contact "Contact1"
         // Delete contact "Contact2",
         // Check that there still contact with name "Contact1"
    }

    @Test
    void testDeleteContactViaGUI(){
         // E2E-test
         // Add contact "Contact1" via GUI
         // Delete contact "Contact1" via GUI
         // Check that there is no contact with text "Contact1" in GUI
    }


//5.2
    //Задание 2. Ниже список тестовых сценариев. Ваша задача - определить тип каждого теста (юнит-тест,
    //интеграционный тест, сквозной тест) и объяснить, почему вы так решили.

    Проверка того, что функция addContact корректно добавляет новый контакт в список контактов". - Это Unit-тест, т.к. проверяется
    одна функция (одно звено) изолировано.


    "Проверка того, что при добавлении контакта через пользовательский интерфейс, контакт корректно
    отображается в списке контактов". - Это пример интеграционного теста, т.к. проверяется совместная работа нескольких модулей (звеньев).
    В зависимости от реализации можно считать этот тест - примером E2E теста, т.к. проверяется работа многих модулей через пользовательский интерфейс.


    "Проверка полного цикла работы с контактом: создание контакта, его редактирование и
    последующее удаление - это пример сквозного теста (E2E-test), т.к. проверяется реальная работа всех модулей на уровне пользователя
