# Docker file nodejs azure app services
FROM node:latest
# Create app directory
WORKDIR /app
# Install app dependencies
COPY package*.json ./
RUN npm install
# Build app
COPY . .
RUN npx prisma generate
RUN npm run build
# Expose port
EXPOSE 8080
# Start app
CMD [ "npm", "start" ]
