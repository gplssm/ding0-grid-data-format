# A new data format for ding0 grid data

---

## Reviewing CSV data format developed by Jonas

---
@snap[north span-60]
### HV/MV Transformers
@snapend

@snap[south span-100 text-08]
<table>
<thead>
<tr><th>name      </th><th>description                      </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id        </td><td>unambiguous unique numer         </td><td>integer       </td></tr>
<tr><td>run_id    </td><td>time and date of table generation</td><td>yyyyMMddhhmmss</td></tr>
<tr><td>geom      </td><td>geometric coordinates            </td><td>WGS84 POINT   </td></tr>
<tr><td>name      </td><td>FIXME                            </td><td>string        </td></tr>
<tr><td>voltage_op</td><td>FIXME                            </td><td>float         </td></tr>
<tr><td>s_nom     </td><td>nominal apparent power as float  </td><td>kVA           </td></tr>
<tr><td>x         </td><td>as float                         </td><td>Ohm           </td></tr>
<tr><td>r         </td><td>as float                         </td><td>Ohm           </td></tr>
</tbody>
</table>
@snapend
