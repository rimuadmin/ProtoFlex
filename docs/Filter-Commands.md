# Filter Commands

## SET BANDWIDTH

Set slice filter bandwidth.

```
C[D]<seq_number>|filt <slice_index> <low> <high>
```

**Parameters:**
- `<slice_index>` = slice number
- `<low>` = low cut frequency in Hz
- `<high>` = high cut frequency in Hz

**Example:**
```
C170|filt 0 100 3000
```