# who is it

## Descripción
Someone just sent you an email claiming to be Google's co-founder Larry Page but you suspect a scam.
Can you help us identify whose mail server the email actually originated from?
Download the email file [here](https://artifacts.picoctf.net/c/499/email-export.eml). 
Flag: picoCTF{FirstnameLastname}

## Pistas
- whois can be helpful on IP addresses also, not only domain names

## Solución
```bash
┌──(kali㉿kali)-[~/picoctf]
└─$ cat email-export.eml 
Delivered-To: francismanzi@gmail.com
Received: by 2002:ab0:638a:0:0:0:0:0 with SMTP id y10csp123720uao;
        Thu, 7 Jul 2022 23:19:48 -0700 (PDT)
X-Google-Smtp-Source: AGRyM1u8MgQ0wT0JmPs4nZbKyuwluXeP+mglR/hb66VElgQnwB8M2ofwYUFsHj+eMYBFAVDPITJc
X-Received: by 2002:a5d:6d06:0:b0:21b:c434:d99e with SMTP id e6-20020a5d6d06000000b0021bc434d99emr1524437wrq.148.1657261188086;
        Thu, 07 Jul 2022 23:19:48 -0700 (PDT)
ARC-Seal: i=1; a=rsa-sha256; t=1657261188; cv=none;
        d=google.com; s=arc-20160816;
        b=FJZQS4geDnyabQ7SUhA2v3roEqcufLmysXkLoRZd3yNXiNQFBFmwm5v5yANvDyyebA
         Jfjqv5X8Gujll585xj/MHlVhlEMg0edNWuwnLXj8SmNuPI1Jon9N+fokhSMxy2WxSACE
         4MruPo5QBlHdrFq8WNBAFgC1VtO0nR+BQYY18wqotLIQPvkXo3yOUUhx0D+ZjUwXvTKV
         yUFGdYulF58Lg7wAH/cLWROIHrraWTSsmaGWoYv577nztzueoG5RC5uUAGIAyzsJRqsV
         dCsapFxCUlbYbAgIVraylksCA+veFXfil6ocym8KKnls3j40Vojv0VLhHHZxXruG5x/K
         M5cQ==
ARC-Message-Signature: i=1; a=rsa-sha256; c=relaxed/relaxed; d=google.com; s=arc-20160816;
        h=mime-version:message-id:date:subject:to:from:dkim-signature;
        bh=RneTbuEOZUlwei4ZNPvzjmZpQE92irBmuzImA33zPEc=;
        b=RUd+ycq1YWbRNn9wB8UgJ8dZz0tHpvmqcEGQkWqzLy/6j3aFzaf7dwdoCtXjTTtrrE
         z9g498cmB55fs0x1CAjtzI+Nctb1cbPcnfMCrfsF3LwgYhCErFRnbBbOgqw4eeEB+hk0
         sKBN0QVpSLs1HlF8ZK3XiMKA2p3vSgHlbhMDPGnFTLHEQjlM63d/L30Rt8mpQsT77ni/
         f6X0TqTi4Y8ARIuEELMa6m5E5wQcfUxeUU5WAssz46tQyHKR6xg/g8K2zES+gSNymASk
         c5Eaq55k4Zi8dXWaPIwg4IdhVLVxe4llMx8c46GTdh8tvdMtmjME3wIaFR6Q2SLWRSZA
         o0hw==
ARC-Authentication-Results: i=1; mx.google.com;
       dkim=pass header.i=@onionmail.org header.s=jan2022 header.b=4sU2nk5Z;
       spf=pass (google.com: domain of lpage@onionmail.org designates 173.249.33.206 as permitted sender) smtp.mailfrom=lpage@onionmail.org;
       dmarc=pass (p=NONE sp=NONE dis=NONE) header.from=onionmail.org
Return-Path: <lpage@onionmail.org>
Received: from mail.onionmail.org (mail.onionmail.org. [173.249.33.206])
        by mx.google.com with ESMTPS id f16-20020a05600c4e9000b003a1947873d6si1882702wmq.224.2022.07.07.23.19.47
        for <francismanzi@gmail.com>
        (version=TLS1_3 cipher=TLS_AES_256_GCM_SHA384 bits=256/256);
        Thu, 07 Jul 2022 23:19:47 -0700 (PDT)
Received-SPF: pass (google.com: domain of lpage@onionmail.org designates 173.249.33.206 as permitted sender) client-ip=173.249.33.206;
Authentication-Results: mx.google.com;
       dkim=pass header.i=@onionmail.org header.s=jan2022 header.b=4sU2nk5Z;
       spf=pass (google.com: domain of lpage@onionmail.org designates 173.249.33.206 as permitted sender) smtp.mailfrom=lpage@onionmail.org;
       dmarc=pass (p=NONE sp=NONE dis=NONE) header.from=onionmail.org
DKIM-Signature: v=1; a=rsa-sha256; c=relaxed/relaxed; d=onionmail.org;
 q=dns/txt; s=jan2022; bh=RneTbuEOZUlwei4ZNPvzjmZpQE92irBmuzImA33zPEc=;
 h=from:subject:date:message-id:to:mime-version:content-type;
 b=4sU2nk5ZG4F9+lCtCPU4nat6ovALqfOHOUM1/wTskeMdmMAa2yOMXy0GkqolIioL8nG0mRG45
 OD8b/nHZZEiA0aQppYHECSmXE7IFIFm/MP9wmXIlC/cDF1t9mEwumdDbes7hRhiO6q3A0wYWK+J
 C+qwHI99irsPhWZOptVVh0HV/HJPAtkzg7OBMX/oPDUSG3xo7dJvT5MCYUm2+4CBVjvLmEPUVTO
 uuVEU3HjVjumry5zw1H4s+o9jxCOwpT41uL94NM64Aki4+KIlS75W8Uo1YStqciHSHoEPLMvBhK
 OMfwhI02u5oLFbk6ZvmhyK5juc54lGbWgk277N0hB0Aw==
Received: from localhost
 by mail.onionmail.org (ZoneMTA) with API id 181dc76dff2000ccee.001
 for <francismanzi@gmail.com>;
 Fri, 08 Jul 2022 06:19:47 +0000
X-Zone-Loop: 83440723a48cf749c9e7702024ee772d7cb2fb7cab7a
Content-Type: multipart/mixed; boundary="--_NmP-426c22a2e0d8fc9a-Part_1"
From: Larry Page <lpage@onionmail.org>
To: francismanzi@gmail.com
Subject: One million Prize
Date: Fri, 08 Jul 2022 06:19:47 +0000
Message-ID: <03c11cd1-8fd9-584e-c9d7-e53df0faeccc@onionmail.org>
MIME-Version: 1.0

----_NmP-426c22a2e0d8fc9a-Part_1
Content-Type: multipart/alternative;
 boundary="--_NmP-426c22a2e0d8fc9a-Part_2"

----_NmP-426c22a2e0d8fc9a-Part_2
Content-Type: text/plain; charset=utf-8
Content-Transfer-Encoding: quoted-printable

Hello dear user, I am Larry Page and I am delighted to announce to you that=
 you
are the 99999999th GMAIL account and for that we want to reward you. =
You've
earned $1,000,000. To claim your prize open the attached file.
----_NmP-426c22a2e0d8fc9a-Part_2
Content-Type: text/html; charset=utf-8
Content-Transfer-Encoding: quoted-printable

<p>Hello dear user, I am Larry Page and I am delighted to announce to you =
that you are the 99999999th GMAIL account and for that we want to reward =
you. You've earned $1,000,000. To claim your prize open the attached file.=
<br></p>
----_NmP-426c22a2e0d8fc9a-Part_2--

----_NmP-426c22a2e0d8fc9a-Part_1
Content-Type: text/plain; name=attachment.txt
Content-Transfer-Encoding: base64
Content-Disposition: attachment; filename=attachment.txt

QW1vdW50OiAgJDEsMDAwLDAwMAo=
----_NmP-426c22a2e0d8fc9a-Part_1--
                                                                                                                                            
┌──(kali㉿kali)-[~/picoctf]
└─$ whois 173.249.33.206 | grep person
person:         Wilhelm Zwalina
```

## Bandera
picoCTF{WilhelmZwalina}

## Notas adicionales
| Comando | Descripción |
|--------|--------|
| whois | Es un protocolo de consulta y respuesta gracias al cual es posible consultar bases de datos donde se almacenan los usuarios registrados que están en un recurso de Internet |

## Referencias
[Cómo utilizar comando WHOIS Linux](https://www.solvetic.com/tutoriales/article/8799-como-utilizar-comando-whois-linux-para-que-sirve-usar-e-instalar/)