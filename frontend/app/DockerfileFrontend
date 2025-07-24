# Kullanılacak temel imaj
FROM node:18-alpine

# Uygulama dosyalarının yerleştirileceği klasör
WORKDIR /app

# package.json ve package-lock.json'u kopyala
COPY package*.json ./

# Gerekli kütüphaneleri yükle
RUN npm install

# Tüm frontend dosyalarını kopyala
COPY . .

# Uygulama derlemesi (production için)
RUN npm run build

# Uygulama hangi portu dinleyecek?
EXPOSE 3000

# Uygulama çalıştırma komutu
CMD ["npm", "start"]
