# Zebra-Printer_Link-OS_Get Host Status by Command
# プリンタのホストステータスを取得するコマンド

<img width="500" src="https://images.unsplash.com/photo-1551590192-8070a16d9f67?q=80&w=1471&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
</br>
</br>

プリンタのステータス情報を取得するにあたって、代表的なコマンドが2つある。プリンタの死活監視やオーソドックスなステータス情報収集に用いられる。
</br>

## ■ ZPL:~HS

プリンタの一般的なステータス情報を取得。割り込み型の処理。

```
~HS
159,0,0,0364,000,0,0,0,000,0,0,0
000,0,0,0,0,1,4,0,00000000,1,000
0000,0
```

設定項目の詳細はZPL2 コマンドリファレンスを参照のこと
[~HS.pdf](~HS.pdf)

</br>
</br>

## ■ SGD:device.host_status

~HSと同等情報を収集可能。

```
! U1 getvar "device.host_status"
"159,0,0,0364,000,0,0,0,000,0,0,0
000,0,0,0,0,1,4,0,00000000,1,000
0000,0"
```

設定項目の詳細はZPL2 コマンドリファレンスを参照のこと
[device_host_status.pdf](./device_host_status.pdf)
