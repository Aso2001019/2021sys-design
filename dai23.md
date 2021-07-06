```stsrtuml
@startuml
package "ECサイト" as target_system {
    entity "顧客マスタ" <m_customers><<M,DDAA00>> {
        + customer_code [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
    }
    entity "購入テーブル" <m_customers> <<T,00AADD>> {
        + customer_code [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
    }
  }
@enduml
```
