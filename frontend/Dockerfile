# Builder stage - build the app (create the build folder)
FROM node:alpine as builder

WORKDIR /app

COPY package.json .

RUN npm install

COPY . . 

RUN npm run build

# Build a completely new image with nginx and copy the build folder from the builder stage in usr/share/nginx/html
FROM nginx

COPY --from=builder /app/build /usr/share/nginx/html