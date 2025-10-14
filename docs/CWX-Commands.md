
# CWX Commands

CWX commands manage the CW text buffer for automated CW transmission.

## ERASE

Erase characters from the CW buffer.

```
C[D]<seq_number>|cwx erase <num_chars> [<radio_index>]
```

**Parameters:**
- `<num_chars>` = number of characters to erase
- `<radio_index>` = optional radio index

**Example:**
```
C70|cwx erase 5
C71|cwx erase 3 1
```

## INSERT

Insert text into the CW buffer at a specific position.

```
C[D]<seq_number>|cwx insert <radio_index> "<message>" <block>
```

**Parameters:**
- `<radio_index>` = radio index
- `<message>` = text message to insert
- `<block>` = block number

**Example:**
```
C72|cwx insert 1 "CQ CQ DE W1AW" 0
```

## MACRO SEND

Send a stored CW macro by index.

```
C[D]<seq_number>|cwx macro send <index>
```

**Parameters:**
- `<index>` = macro number to send

**Example:**
```
C73|cwx macro send 1
```

## SEND

Send CW text message.

```
C[D]<seq_number>|cwx send "<message>" <block>
```

**Parameters:**
- `<message>` = text message to send
- `<block>` = block number

**Example:**
```
C74|cwx send "73 DE W1AW" 0
```