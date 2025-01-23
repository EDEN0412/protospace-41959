## テーブル設計

### users テーブル

| カラム名          | 型        | オプション           |
|-------------------|-----------|----------------------|
| email             | string    | NOT NULL, UNIQUE     |
| encrypted_password| string    | NOT NULL             |
| name              | string    | NOT NULL             |
| profile           | text      | NOT NULL             |
| occupation        | text      | NOT NULL             |
| position          | text      | NOT NULL             |

### prototypes テーブル

| カラム名          | 型        | オプション           |
|-------------------|-----------|----------------------|
| title             | string    | NOT NULL             |
| catch_copy        | text      | NOT NULL             |
| concept           | text      | NOT NULL             |
| user              | references| NOT NULL, Foreign Key|

### comments テーブル

| カラム名          | 型        | オプション           |
|-------------------|-----------|----------------------|
| content           | text      | NOT NULL             |
| prototype         | references| NOT NULL, Foreign Key|
| user              | references| NOT NULL, Foreign Key|
