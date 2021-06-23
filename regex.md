# Regeular Expression - Regex Collection

---
### Currency format with comma

Expression: 
`^(\d{1,3})(,\d{1,3})*(\.\d{1,})?$`

Samples: 
`123                   `
`1,111                 `
`11,234                `
`234,678               `
`1,111,444             `
`6666,7777,888         `
`777777777777777777.77 `
`1.2                   `
`2.55                  `

---
### Similar Surnames

Expression:
`Joh?n(athan)?`

Samples:
`Jonathan `
`John     `
`Jon      `
`Johnathan`

---
### Similar Surnames

Expression:
`Joh?n(athan)?`

Samples:
`Jonathan `
`John     `
`Jon      `
`Johnathan`

---
### Static Files URL

Expression:
`http://.+$(?<!\.gif|\.png|\.css|\.js)`

Samples:
`http://ads/fff.jpg        `
`http://FDD/               `
`http://a.gif              `
`http://ASD/jfss/ghfs24.png`
`http://adf/test.jss       `

---
### Remove Empty CSV Fields

Expression:
`\s*,\s*,`

Samples:
`,,   ,, ,,  ,,                                               `

`,, ,   ,,                                                    `

`,  ,   ,                                                     `

`,,   ,,   ,,,        ,Heap Usage,,%JVM Utilization,,,,,,,,, ,`

Java Solution:
`test = (test.replaceAll("\\s*,\\s*,", ",")).replaceAll("\\s*,\\s*,", "").replaceAll(",\\s*$", "");`


---
### Multiple Fragment of text 

Expression:
`^(?!.*(<RespCode>success</RespCode>|>000<actCode>)).*$`

Samples:
`abc<RespCode>succe</RespCode>aa  `

`abc<RespCode>success</RespCode>aa`

`aaa>000<actCode>                 `

`aaa>00<actCode>                  `

`rrrrrrrrr                        `

`8888888 aaa>00<actCode>          `


