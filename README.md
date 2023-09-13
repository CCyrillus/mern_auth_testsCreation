                        Documentation and setup instructions


                          Data Modeling and ERD Diagrams for User app
      +-------------------------+
      |      User               |
      +-------------------------+
      | _id: String             |
      | firstName: Array<Object>|
      | lastName: String        |
      | email: String           |
      | password: String        |
      | pisturePath: String Ref |
      | location: String        |
      | ocupation: String       |
      | viewedProfile: Number   |
      | impressions: Number     |
      | scores: Number          |
      +-------------------------+
            |
            |
            | 1
            |
            |
      +-----------------------------+
      |      Post                   |
      +-----------------------------+
      | _id: String Ref             |
      | firstName: String           |
      | lastName: String            |
      | userId: String Ref          |
      | location: String            |
      | description: String         |
      | userPicturePath: String Ref |
      | pisturePath: String Ref     |
      | likes: Object<String Ref>   |
      | comments:Array<String>      |
      +-----------------------------+
            |
            |
            | N
            |
            |
      +-----------------------------+
      |    Friend(Sub Doc)          |
      +-----------------------------+
      | _id: String Ref             |
      | firstName: String           |
      | lastName: String            | 
      | pisturePath: String Ref     |
      | location: String            |
      | ocupation: String           |
      +-----------------------------+
            |
            |
            | N
            |
            |
      +------------------+
      |       Images     |
      +------------------+
      |      path        |
      +------------------+
      
                        Data Modeling and ERD Diagrams for testsCreation

      +-------------------------+
      |      User               |
      +-------------------------+
      | _id: String             |
      | firstName: Array<Object>|
      | lastName: String        |
      | email: String           |
      | password: String        |
      | pisturePath: String Ref |
      | location: String        |
      | ocupation: String       |
      | viewedProfile: Number   |
      | impressions: Number     |
      | scores: Number          |
      +-------------------------+
            |
            |
            | 1
            |
            |
      +------------------------------+
      |      Test                    |
      +------------------------------+
      | _id: String Ref              |
      | userId: String Ref           |
      | title: String                ! // название теста
      ! questions: Array<Object>     | // вопросы в тесте
      | description: String          | // описание теста
      +------------------------------+
            |
            |
            | N
            |
            |
      +------------------------+
      |    Question            |
      +------------------------+
      | _id: String Ref        |
      | text: String           | // текст вопроса
      | options: Array<String> | // варианты ответов
      +------------------------+
            |
            |
            | N
            |
            |
      +------------------+
      | AssessmentResult |
      +------------------+
      | _id: String Ref  |
      | testId: String   | // дентификатор теста, к которому относится результат
      | userId: String   | // идентификатор пользователя, чей результат
      | score: Number    | // баллы за тест
      +------------------+




     