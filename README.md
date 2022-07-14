# Buffer Class

Allocate
```ahk
buffer := buffer(30)

buffer := buffer_from("aGVsbG8gd29ybGQ=", "base64")
MsgBox % "from base64: " buffer.toString()

buffer := buffer_from("68656C6C6F20776F726C64", "hex")
MsgBox % "from hex: " buffer.toString()

buffer := buffer_from("hello world")
MsgBox % "from string: " buffer.toString()
```

to String
```ahk
MsgBox % "string: " buffer.toString()
MsgBox % "base64 string: " buffer.toString("base64")
MsgBox % "hex string: " buffer.toString("hex")
```

Enumerate
```ahk
for offset, byte in buffer
    MsgBox % offset ": " byte
```

Byte get/set
```ahk
byte := buffer[offset]
buffer[offset] := byte
```

File read/write
```ahk
buffer := buffer_fromFile("output.bin")
buffer.save("output.bin")
```

## Buffer Class
- `buffer := buffer(length, fillByte="", encoding="utf-8")`
- `buffer := buffer_from(buffer, [offset], [length])`
- `buffer := buffer_from(string, [encoding])`
    - `encoding` `encoding | "base64" | "hex"`
- `buffer := buffer_fromFile(path, [offset], [length])`
- `buffer.toString([encoding], [offset], [length])`
    - `encoding` `encoding` | `"base64"` | `"hex"`
- `buffer.fill([value], [offset], [length])`
- `buffer.write(data, [offset], [length], [encoding])`
- `buffer.save(path, [offset], [length]))`
- `buffer.ptr`
- `buffer.length`
- `buffer.encoding`
- `buffer[offset]` `byte`

## Contact
[카카오톡 오픈 프로필](https://open.kakao.com/me/neovis)
