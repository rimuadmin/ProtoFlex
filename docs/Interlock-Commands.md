Configure transmit interlock parameters.

```
C[D]<seq_number>|interlock <parameter>=<value>
```

**Available Parameters:**

| Parameter | Value Range | Description |
|-----------|-------------|-------------|
| `acc_tx_delay` | `ms` | Set ACC TX delay in milliseconds |
| `acc_tx_enabled` | `0\|1` | Enable/disable ACC TX |
| `acc_txreq_enable` | `0\|1` | Enable/disable ACC TX request |
| `acc_txreq_polarity` | `0\|1` | Set ACC TX request polarity |
| `rca_txreq_enable` | `0\|1` | Enable/disable RCA TX request |
| `rca_txreq_polarity` | `0\|1` | Set RCA TX request polarity |
| `timeout` | `ms` | Set interlock timeout in milliseconds |
| `tx_delay` | `ms` | Set general TX delay in milliseconds |
| `tx1_delay` | `ms` | Set TX1 delay in milliseconds |
| `tx1_enabled` | `0\|1` | Enable/disable TX1 |
| `tx2_delay` | `ms` | Set TX2 delay in milliseconds |
| `tx2_enabled` | `0\|1` | Enable/disable TX2 |
| `tx3_delay` | `ms` | Set TX3 delay in milliseconds |
| `tx3_enabled` | `0\|1` | Enable/disable TX3 |

**Examples:**
```
C190|interlock acc_tx_delay=100
C191|interlock acc_tx_enabled=1
C192|interlock tx_delay=50
C193|interlock timeout=5000
```