FROM node:20-alpine

WORKDIR /app

COPY backend/package*.json ./

RUN npm install

COPY src ./src
COPY db ./db

ENV NODE_ENV=production
ENV PORT=4500
ENV DB_DIR=/app/db

EXPOSE 4500

CMD ["node","src/index.js"]
