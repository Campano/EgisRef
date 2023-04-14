<!--
 ___ _            _ _    _ _    __
/ __(_)_ __  _ __| (_)__(_) |_ /_/
\__ \ | '  \| '_ \ | / _| |  _/ -_)
|___/_|_|_|_| .__/_|_\__|_|\__\___|
            |_| 
-->
![](https://docs.simplicite.io//logos/logo250.png)
* * *

`Referentiel` module definition
===============================



`RefCpc` business object definition
-----------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `refCpcCode`                                                 | char(255)                                | yes*     | yes       |          | -                                                                                |
| `refCpcLabel`                                                | char(255)                                | yes      | yes       |          | -                                                                                |
| `refCpcSrvId` link to **`RefServiceLine`**                   | id                                       |          | yes       |          | -                                                                                |
| _Ref. `refCpcSrvId.refSrvLabel`_                             | _char(100)_                              |          |           |          | -                                                                                |

`RefServiceLine` business object definition
-------------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `refSrvLabel`                                                | char(100)                                | yes*     | yes       |          | -                                                                                |
| `refSrvState`                                                | enum(20) using `REF_SRV_STATE` list      | yes      | yes       |          | -                                                                                |

### Lists

* `REF_SRV_STATE`
    - `DRAFT` Draft
    - `VALIDATED` Validated

