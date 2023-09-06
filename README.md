      +----------------------+
      |      User            |
      +----------------------+
      | _id: String (PK)     |
      | firstName: String    |
      | lastName: String     |
      | email: String        |
      | password: String     |
      | scores: Number       |
      | picturesPath: String |
      +----------------------+
            |
            |
            | 1
            |
            |
      +------------------------------+
      |      Test                    |
      +------------------------------+
      | _id: String (PK)             |
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
      | _id: String (PK)       |
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
      | _id: String (PK) |
      | testId: String   | // дентификатор теста, к которому относится результат
      | userId: String   | // идентификатор пользователя, чей результат
      | score: Number    | // баллы за тест
      +------------------+