# Usa una imagen base oficial de Node
FROM node:18

# Instala dependencias necesarias para React Native + Expo
RUN apt-get update && apt-get install -y \
  git \
  python3 \
  make \
  curl \
  default-jdk \
  && rm -rf /var/lib/apt/lists/*


# Crea directorio de trabajo
WORKDIR /app

# Instala expo-cli de forma global
RUN npm install -g expo-cli

# Expone el puerto para desarrollo de Expo
EXPOSE 19000 19001 19002

# Punto de entrada por defecto al iniciar el contenedor
CMD ["bash"]
