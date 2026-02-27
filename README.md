# 1key-tls-repository
One click deployment of an image repository based on Docker Registry 2, supporting TLS and htpasswd authentication

## Usage

    $ ./deploy.sh
    用法: ./deploy.sh <密码> [仓库地址]
    示例:
    ./deploy.sh 123456                    # 使用 hostname.local 作为域名
    ./deploy.sh 123456 myregistry.local   # 使用指定域名（FQDN）
    ./deploy.sh 123456 myhost              # 短名，自动补 .local
    ./deploy.sh 123456 192.168.1.100       # 使用指定 IP，域名取 hostname.local

仓库地址可以是 IP 或域名（FQDN 或短名），用于CA证书SAN属性的域名和ip地址，docker 客户端访问仓库时使用

