FROM node:14.16.1

WORKDIR /usr/src/app/frontend
COPY frontend/package.json frontend/package-lock.json ./
RUN npm install

COPY frontend/ .

WORKDIR /usr/src/app/backend
COPY backend/package.json backend/package-lock.json ./
RUN npm install

COPY backend/common ./common

WORKDIR /usr/src/app/frontend

EXPOSE 3002
CMD ["npm", "run", "start"]