FROM node:12-alpine
WORKDIR /listener
COPY package*.json ./
COPY . .
RUN npm install --production && npm install -g @vercel/ncc && ncc build index.js -o dist && rm -rf node_modules
EXPOSE 3001
CMD ["node", "dist/index.js"]