# MyBasicSQL

# Создание vw запроса

CREATE VIEW vw_account_and_status AS
  SELECT a.id_account,
    a.account_number,
    a.last_name, a.name,
    a.id_account_status,
    s.account_status
  FROM `account` AS a
    INNER JOIN account_status AS s
      ON s.id_account_status =
        a.id_account_status;

