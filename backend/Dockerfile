# Использование образа Node.js версии 14.16.1
FROM node:14.16.1
# Указываем директорию внутри контейнера, с которой работаем
WORKDIR /usr/src/app/backend
# Копируем файлы в папку выше
COPY package.json package-lock.json ./
#  устанавливает все зависимости Node.js, указанные в package.json во время сборки образа
RUN npm install
# Копируем из текущей в текущую в контейнере
COPY . .
# Назначаем порт 3001 
EXPOSE 3001
# Команда для запуска приложения
CMD [ "npm", "run", "start" ]