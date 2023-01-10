Нужно сгенерировать сертификат, для этого нужно прописать команду 
(для linux)

go run /usr/local/go/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost

Для винды или мака +- то же самое, нужно смотреть GOROOT