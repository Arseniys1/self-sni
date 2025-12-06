# Генерируем приватный ключ
openssl genrsa -out ssl/key.pem 2048

# Генерируем самоподписанный сертификат
openssl req -new -x509 -key ssl/key.pem -out ssl/cert.pem -days 365 -subj "/C=US/ST=State/L=City/O=Organization/CN=your-domain.com"
