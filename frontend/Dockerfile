# Используем официальный образ Node.js в качестве базового
FROM node:16-alpine

# Устанавливаем рабочую директорию в контейнере
WORKDIR /app

# Копируем package.json и package-lock.json в контейнер
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем все файлы и каталоги проекта в контейнер
COPY . .

# Сборка приложения для продакшн
RUN npm run build

# Указываем команду запуска сервера
CMD ["npm", "run", "start"]

# Экспонируем порт, на котором приложение будет доступно
EXPOSE 3000

