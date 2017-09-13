# module: selenium.webdriver.common.alert
# class Alert(driver)

alert = self.driver.switch_to_alert()

---

| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| text  | Gets the text of the Alert  |   | alert.text |
| dismiss  | Dismisses the alert available  |   |  alert.dismiss() |
| accept  | Accepts the alert available  |   |  alert.accept() |
| send_keys  | Send Keys to the Alert  | *keysToSend:* Any character.  |  alert.send_keys() |

---
