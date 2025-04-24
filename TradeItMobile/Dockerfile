# Usa una imagen base oficial de Node
FROM node:18

# Instala dependencias necesarias del sistema
RUN apt-get update && apt-get install -y \
  git \
  python3 \
  make \
  curl \
  default-jdk \
  && rm -rf /var/lib/apt/lists/*

# Crea el directorio de trabajo
WORKDIR /app

# Copia solo los archivos de dependencias
COPY package*.json ./

# Instala Expo CLI globalmente
RUN npm install -g expo-cli

# Instala dependencias locales (solo si no montas volumen, si no, lo hace CMD)
# RUN npm install

# Copia el resto del código (opcional si montas volumen en docker-compose)
# COPY . .

# Expone puertos para Expo Web (19006)
EXPOSE 19006

# Comando para instalar dependencias y lanzar modo web
CMD ["sh", "-c", "npm install && npm run web"]
