##facebook-clone

Requirements

## Functional
- Users can share, like,comments,update,delete post
- Users can add and remove friends
- Users can change post access to public/private
- Users can see news feeds
- Users can search for friends
- Users can share profile
- User can delete account

## Non-Functional
- Application should be secure
_ Application should be available

## Database Design
- POST
    - id: bigint,autoincrement,primary
    - text: text
    - author:   USER 
    - created_on: datetime
    - updated_on: datetime

- POST-MEDIA
    - id: bigint
    - file: varchar(url)
    - post: POST
    - created_on: datetime
    - updated_on: datetime

- USER
    - id: bigInt, autoincrement, primary
    - username: varchar
    - email: varchar
    - created_on: datetime
    _ updated_on: datetime

- PROFILE
    - id: bigint,autoincrement,primary
    - owner: USER
    - image: varchar(url)
    - address: ADDRESS
    - created_on: datetime
    - updated_on: datetime
    
- COMMENT
    - id: bigint,autoincrement,primary
    - text: text
    - author:   USER 
    - created_on: datetime
    - updated_on: datetime
    
- LIKE
    - id: bigint,autoincrement,primary
    - post: POST
    - owner: USER
    - created_on: datetime
    - updated_on: datetime
    
## FOR LATER
- FRIEND
    - id: bigint,autoincrement,primary
    - user: USER
    - created_on: datetime
    - updated_on: datetime

- ADDRESS
    - id: bigint,autoincrement,primary
    - zip_code
    _ country:
    - created_on: datetime
    - updated_on: datetime

## API DESIGN
- [GET, POST, PUT, PATCH, DELETE]
- [GET_LIST, GET_ONE, CREATE, UPDATE_ALL, UPDATE_SOME, DESTROY]
- POSTS, USERS, COMMENTS, LIKE, FRIENDS

## APP STRUCTURE
- POST
    - POST_MEDIA
    - LIKE
    - COMMENT
    
- USER
    - FRIEND
    - PROFILE
    
    
- USER
- POSTS
    - GET_LIST: returns a list of posts
        - URL: /api/v1/posts
        - METHOD: GET
        - REQUEST
            - HEADERS: Authorization
            - BODY:
            
        - RESPONSE:
            - HEADERS: Authorization
            - BODY: {
                id: int,
                text: str,
                created-on: datetime
                author: user
            }
        












