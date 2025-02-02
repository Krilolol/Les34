# Les34

AWS - Jenkins
1. Налаштувати EC2 серверів.
- За допомогою terraform створив 3 сервери: app, jenkins-master та jenkins-worker;
![1](https://github.com/user-attachments/assets/8d5ec893-048c-45cf-b899-03cfb98154f9)

- За допомогою ansible на jenkins-master встановлюю Jenkins, на jenkins-worker - Java, на app - docker та docker-compose;
![2](https://github.com/user-attachments/assets/a2a0ff63-ec2e-4102-b231-93482595a1f7)
![3](https://github.com/user-attachments/assets/7c10a9e6-041e-429b-8739-e90c273bc148)
![4](https://github.com/user-attachments/assets/8dd18f7a-4466-4e41-8287-4777ed88775e)


2. Деплой та налаштування Jenkins.

    Встановлення плагинів та налаштування jenkins-master
   ![5](https://github.com/user-attachments/assets/db206ef3-e1c2-458e-839a-4b2317a88841)
   ![6](https://github.com/user-attachments/assets/39005a45-06ba-49aa-afef-91e23646c3ce)
   ![7](https://github.com/user-attachments/assets/400df1db-f00a-4697-95f5-f5f74295ac1e)

    Налаштування jenkins-worker та під'єднання його до jenkins-master
![8](https://github.com/user-attachments/assets/275d6b0d-c620-4c0d-8c1e-23ebc8e1b958)

3. Налаштувати Freestyle Job.

    Налаштував СІ для репозиторія з проєктом на GitLab - [https://gitlab.com/krilolol/catalogbooks]
   ![9](https://github.com/user-attachments/assets/3de8e29a-9cd9-476b-a379-e619017be45f)
![10](https://github.com/user-attachments/assets/c745c611-48d8-4393-a0f0-2119d22740fc)

    Налаштував СD, в результаті чого запустилося 4 контейнери (frontend для каталогу книг, pg-admin для адміністрування postgres)
   ![11](https://github.com/user-attachments/assets/e7acc002-f133-4fea-baaf-f2a6855fea65)
![12](https://github.com/user-attachments/assets/ca6007de-5eb3-4485-8989-7053efcad86f)
![13-2](https://github.com/user-attachments/assets/b9a39de8-cca6-4473-98d3-118a8f479392)

    Скрипт для запуску додатку:
   
![изображение](https://github.com/user-attachments/assets/e5128cc6-4b62-452e-a2fc-916114e27ec9)
   
5. Налаштування декларативного пайплайну
- У файлі deploy.Jenkinsfile описав налаштування для CI/CD. Як результат запустився додаток
![15](https://github.com/user-attachments/assets/f369618c-2f7f-45df-bd16-579323aad59e)
