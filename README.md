
# Todo API

## 구현 기능

- Todo 생성하기           `POST /tasks`
    - Request
      ```json
      {
          "content": "content of todo"
      }
      ```
    - Response
      ```text
      HttpStatus.CREATED
      ```

- Todo 수정하기           `PATCH /tasks/{todoTaskId}`
    - Request
      ```json
      {
        "isChecked": "whether todo has been checked",
        "updatedAt": "2022-02-08 13:40:17"
      }
      ```
    - Response
      ```text
      HttpStatus.NO_CONTENT	 
      ```

- Todo 삭제하기           `DELETE /tasks/{todoTaskId}`
	-  Request
	      ```json
	      {
	        "isDeleted": "whether todo has been deleted"
	        "deletedAt": "2022-02-08 13:40:17"
	      }
	      ```
    - Response
      ```text
      HttpStatus.NO_CONTENT
      ```

- 모든 Todo 조회하기       `GET /tasks`
    - Response
    ```text
    HttpStatus.OK
    ```
    ```json
    {
      "todos": [
          {
              "id": 1,
              "content": "content of memo",
              "isChecked": "whether todo has been checked"
              "createdAt": "2022-02-08 13:40:17"
              "updatedAt": "2022-02-08 13:40:17"
              "deletedAt": "2022-02-08 13:40:17"
          }
      ]
    }
    ```
