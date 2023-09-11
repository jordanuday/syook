FROM node:12-alpine
WORKDIR /emitter
COPY package*.json ./
COPY . .
RUN npm install --production && npm install -g @vercel/ncc && ncc build index.js -o dist && rm -rf node_modules
CMD ["node", "dist/index.js"]