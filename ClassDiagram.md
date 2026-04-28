```mermaid
classDiagram
    class User {
        -id : String
        -pw : String
        -name : String
        -phone : String
        -address : String
        +registerUser(id: String,pw: String,name: String, phone: String, address: String) boolean
        +updateUser(id: String,name: String, phone: String, address: String) boolean
        +deleteUser(id: String) boolean
        +searchUser(id: String) boolean
    }

    class Account {
        -number : String
        -balance : double
        +deposit(userId: String, amount: double) double
        +withdraw(userId: String, amount: double) double
        +transfer(userId: String, targetNumber: String, amount: double) double
        +computeBalance() double
    }

    Account "1..*" --> "1" User : 사용자조회
