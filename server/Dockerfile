# stage 1
FROM node:23-alpine AS builder

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npx prisma generate
RUN npm run build

# stage 2
FROM node:23-alpine AS runner

WORKDIR /app

# Copy necessary files from the builder stage
COPY --from=builder /app/package.json ./package.json
COPY --from=builder /app/dist ./dist
COPY --from=builder /app/prisma ./prisma

# Install production dependencies
RUN npm install --production

EXPOSE 8080

CMD ["npm", "start"]