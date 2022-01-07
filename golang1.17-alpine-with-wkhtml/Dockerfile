FROM surnet/alpine-wkhtmltopdf:3.10-0.12.5-full as wkhtmltopdf
FROM golang:1.17-alpine AS BUILDER

COPY --from=wkhtmltopdf /bin/wkhtmltopdf /usr/local/bin/wkhtmltopdf
COPY --from=wkhtmltopdf /bin/wkhtmltoimage /usr/local/bin/wkhtmltoimage
COPY --from=wkhtmltopdf /bin/libwkhtmltox* /usr/local/bin/

RUN apk add --no-cache g++ libx11 libxrender libxext fontconfig freetype