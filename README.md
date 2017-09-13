# Bencode

Bencode is a general purpose bencode encoder & decoder written in swift 4.

Inspired by [VFK SwiftyBencode][vfk] & [arvidsigvardsson/Bencode][abc]

## Usage

**Initialize with URL:**

```swift
let bencode: Bencode? = Bencode(file: torrentUrl)
```

**Initialize with bencoded string:**

```swift
let bencode: Bencode? = Bencode(bencodedString: content)
```

**Accessing properties:** 

Accessing properties is very handy with subscripts & value accessors.
Value accessors `.int` & `.string` are optional. 
Subscripts produces **BencodeOptional** enums (providing the same accessors like subscripts & value types), by doing so you can chain optional subscripts without having to write `?` or `!` behind every one of them.

```swift
let filePath: String? = bencode["info"]["files"][0]["path"][0].string
let fileLength: Int? = bencode["info"]["files"]["length"].int
```

## Help

* Post any issues you find
* Post new feature requests
* Pull requests are welcome


[vfk]: https://github.com/VFK/SwiftyBencode
[abc]: https://github.com/arvidsigvardsson/Bencode
