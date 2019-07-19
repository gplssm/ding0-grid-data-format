@snap[midpoint text-08 span-100]
# A new data format for ding0 grid data
@snapend

---

## Reviewing CSV data format developed by Jonas


---
@snap[north span-80]
### lv_grid.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name       </th><th>description                                            </th><th>unit              </th></tr>
</thead>
<tbody>
<tr><td>id         </td><td>unambiguous unique numer                               </td><td>integer           </td></tr>
<tr><td>run_id     </td><td>time and date of table generation                      </td><td>yyyyMMddhhmmss    </td></tr>
<tr><td>id_db      </td><td>unambiguous number of LV-Grid                          </td><td>integer           </td></tr>
<tr><td>name       </td><td>unambiguous name: 'LVGridDing0_LV_#lvgridid#_#lvgridid#</td><td>string            </td></tr>
<tr><td>geom       </td><td>geometric coordinates                                  </td><td>WGS84 MULTIPOLYGON</td></tr>
<tr><td>population </td><td>population in LV-Grid                                  </td><td>integer           </td></tr>
<tr><td>voltage_nom</td><td>voltage level of grid as float                         </td><td>kV                </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### versioning.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name       </th><th>description                      </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id         </td><td>unambiguous unique numer         </td><td>integer       </td></tr>
<tr><td>run_id     </td><td>time and date of table generation</td><td>yyyyMMddhhmmss</td></tr>
<tr><td>description</td><td>Used parameters for this run     </td><td>string        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mv_generator.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name            </th><th>description                                                                                </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id              </td><td>unambiguous unique numer                                                                   </td><td>integer       </td></tr>
<tr><td>run_id          </td><td>time and date of table generation                                                          </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>id_db           </td><td>unambiguous number of MV-Grid                                                              </td><td>integer       </td></tr>
<tr><td>name            </td><td>unambiguous name: 'MVGeneratorDing0_MV_#mvgridid#_#ascendingnumber#'                       </td><td>string        </td></tr>
<tr><td>geom            </td><td>geometric coordinates                                                                      </td><td>WGS84 POINT   </td></tr>
<tr><td>type            </td><td>type of generation: {solar; biomass}                                                       </td><td>string        </td></tr>
<tr><td>subtype         </td><td>subtype of generation: {solar_ground_mounted, solar_roof_mounted, unknown; biomass, biogas}</td><td>string        </td></tr>
<tr><td>v_level         </td><td>voltage level of generator as integer                                                      </td><td>FIXME         </td></tr>
<tr><td>nominal_capacity</td><td>nominal capacity as float                                                                  </td><td>FIXME         </td></tr>
<tr><td>weather_cell_id </td><td>unambiguous number of the corresponding weather cell                                       </td><td>integer       </td></tr>
<tr><td>is_aggregated   </td><td>True if load is aggregated load, else False                                                </td><td>boolean       </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mv_grid.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name       </th><th>description                                             </th><th>unit              </th></tr>
</thead>
<tbody>
<tr><td>id         </td><td>unambiguous unique numer                                </td><td>integer           </td></tr>
<tr><td>run_id     </td><td>time and date of table generation                       </td><td>yyyyMMddhhmmss    </td></tr>
<tr><td>id_db      </td><td>unambiguous number of MV-Grid                           </td><td>integer           </td></tr>
<tr><td>geom       </td><td>geometric coordinates                                   </td><td>WGS84 MULTIPOLYGON</td></tr>
<tr><td>name       </td><td>unambiguous name: 'MVGridDing0_MV_#mvgridid#_#mvgridid#'</td><td>string            </td></tr>
<tr><td>population </td><td>population in MV-Grid                                   </td><td>integer           </td></tr>
<tr><td>voltage_nom</td><td>voltage level of grid as float                          </td><td>kV                </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### lv_generator.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name            </th><th>description                                                         </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id              </td><td>unambiguous unique numer                                            </td><td>integer       </td></tr>
<tr><td>run_id          </td><td>time and date of table generation                                   </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>id_db           </td><td>unambiguous number of LV-Grid                                       </td><td>integer       </td></tr>
<tr><td>la_id           </td><td>FIXME                                                               </td><td>integer       </td></tr>
<tr><td>name            </td><td>unambiguous name: 'LVGeneratorDing0_LV_#lvgridid#_#ascendingnumber#'</td><td>string        </td></tr>
<tr><td>lv_grid_id      </td><td>unambiguous id_db of LV-Grid                                        </td><td>integer       </td></tr>
<tr><td>geom            </td><td>geometric coordinates                                               </td><td>WGS84, POINT  </td></tr>
<tr><td>type            </td><td>type of generation {solar; biomass}                                 </td><td>string        </td></tr>
<tr><td>subtype         </td><td>subtype of generation: {solar_roof_mounted, unknown; biomass}       </td><td>string        </td></tr>
<tr><td>v_level         </td><td>voltage level of generator as integer                               </td><td>FIXME         </td></tr>
<tr><td>nominal_capacity</td><td>nominal capacity as float                                           </td><td>FIXME         </td></tr>
<tr><td>is_aggregated   </td><td>True if load is aggregated load, else False                         </td><td>boolean       </td></tr>
<tr><td>weather_cell_id </td><td>unambiguous number of the corresponding weather cell                </td><td>integer       </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mvlv_transformer.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name      </th><th>description                                        </th><th>unit       </th></tr>
</thead>
<tbody>
<tr><td>id        </td><td>unambiguous unique numer                           </td><td>integer    </td></tr>
<tr><td>run_id    </td><td>time and date of table generation in yyyyMMddhhmmss</td><td>integer    </td></tr>
<tr><td>id_db     </td><td>unambiguous number of LV-Grid                      </td><td>integer    </td></tr>
<tr><td>geom      </td><td>geometric coordinates                              </td><td>WGS84 POINT</td></tr>
<tr><td>name      </td><td>FIXME                                              </td><td>string     </td></tr>
<tr><td>voltage_op</td><td>as float                                           </td><td>kV         </td></tr>
<tr><td>s_nom     </td><td>nominal apparent power as float                    </td><td>kVA        </td></tr>
<tr><td>x         </td><td>as float                                           </td><td>Ohm        </td></tr>
<tr><td>r         </td><td>as float                                           </td><td>Ohm        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### lv_load.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name       </th><th>description                                                                       </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id         </td><td>unambiguous unique numer                                                          </td><td>integer       </td></tr>
<tr><td>run_id     </td><td>time and date of table generation                                                 </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>id_db      </td><td>unambiguous number of LV-Grid                                                     </td><td>integer       </td></tr>
<tr><td>name       </td><td>unambiguous name: 'LVLoadDing0_LV_#lvgridid#_#ascendingnumber#'                   </td><td>string        </td></tr>
<tr><td>lv_grid_id </td><td>unambiguous id_db of LV-Grid                                                      </td><td>integer       </td></tr>
<tr><td>geom       </td><td>geometric coordinates                                                             </td><td>WGS84 POINT   </td></tr>
<tr><td>consumption</td><td>type of load {residential, agricultural, industrial} and corresponding consumption</td><td>string        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### line.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name     </th><th>description                                                                         </th><th>unit            </th></tr>
</thead>
<tbody>
<tr><td>id       </td><td>unambiguous unique numer                                                            </td><td>integer         </td></tr>
<tr><td>run_id   </td><td>time and date of table generation                                                   </td><td>yyyyMMddhhmmss  </td></tr>
<tr><td>id_db    </td><td>unambiguous number of corresponding grid (MVgrid-id if MV-edge, LVgrid-id if LV-edge</td><td>integer         </td></tr>
<tr><td>edge_name</td><td>unambiguous name of edge                                                            </td><td>string          </td></tr>
<tr><td>grid_name</td><td>unambiguous name of grid                                                            </td><td>string          </td></tr>
<tr><td>node1    </td><td>id_db of first node                                                                 </td><td>string          </td></tr>
<tr><td>node2    </td><td>id_db of second node                                                                </td><td>string          </td></tr>
<tr><td>type_kind</td><td>n/a                                                                                 </td><td>string          </td></tr>
<tr><td>type_name</td><td>n/a                                                                                 </td><td>string          </td></tr>
<tr><td>length   </td><td>length of line as float                                                             </td><td>km              </td></tr>
<tr><td>u_n      </td><td>nominal voltage as float                                                            </td><td>kV              </td></tr>
<tr><td>c        </td><td>inductive resistance at 50Hz as float                                               </td><td>uF/km           </td></tr>
<tr><td>l        </td><td>stored as float                                                                     </td><td>mH/km           </td></tr>
<tr><td>r        </td><td>stored as float                                                                     </td><td>Ohm/km          </td></tr>
<tr><td>i_max_th </td><td>stored as float                                                                     </td><td>A               </td></tr>
<tr><td>geom     </td><td>geometric coordinates                                                               </td><td>WGS84 LINESTRING</td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### lv_station.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name  </th><th>description                                        </th><th>unit       </th></tr>
</thead>
<tbody>
<tr><td>id    </td><td>unambiguous unique numer                           </td><td>integer    </td></tr>
<tr><td>run_id</td><td>time and date of table generation in yyyyMMddhhmmss</td><td>integer    </td></tr>
<tr><td>id_db </td><td>unambiguous number of LV-Grid                      </td><td>integer    </td></tr>
<tr><td>geom  </td><td>geometric coordinates                              </td><td>WGS84 POINT</td></tr>
<tr><td>name  </td><td>FIXME                                              </td><td>string     </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### lv_branchtee.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name  </th><th>discription                                                              </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id    </td><td>unambiguous unique numer                                                 </td><td>integer       </td></tr>
<tr><td>run_id</td><td>time and date of table generation                                        </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>geom  </td><td>geometric coordinates                                                    </td><td>WGS84 POINT   </td></tr>
<tr><td>id_db </td><td>unambiguous number of LV-Grid                                            </td><td>integer       </td></tr>
<tr><td>name  </td><td>unambiguous name: 'LVCableDistributorDing0_LV_#lvgridid#_#ascendingnumber</td><td>string        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### hvmv_transformer.json
@snapend

@snap[midpoint span-100 text-04]
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

---
@snap[north span-80]
### mv_branchtee.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name  </th><th>description                                                                </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id    </td><td>unambiguous unique numer                                                   </td><td>integer       </td></tr>
<tr><td>run_id</td><td>time and date of table generation                                          </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>id_db </td><td>unambiguous number of MV-Grid                                              </td><td>integer       </td></tr>
<tr><td>geom  </td><td>geometric coordinates                                                      </td><td>WGS84 POINT   </td></tr>
<tr><td>name  </td><td>unambiguous name: 'MVCableDistributorDing0_MV_#mvgridid#_#ascendingnumber#'</td><td>string        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mv_station.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name  </th><th>description                                               </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id    </td><td>unambiguous unique numer                                  </td><td>integer       </td></tr>
<tr><td>run_id</td><td>time and date of table generation                         </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>id_db </td><td>unambiguous number of MV-Grid                             </td><td>integer       </td></tr>
<tr><td>geom  </td><td>geometric coordinates                                     </td><td>WGS84 POINT   </td></tr>
<tr><td>name  </td><td>unambiguous name: 'LVStationDing0_MV_#mvgridid#_#lvgridid#</td><td>string        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mv_circuitbreaker.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name  </th><th>description                      </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id    </td><td>unambiguous unique numer         </td><td>integer       </td></tr>
<tr><td>run_id</td><td>time and date of table generation</td><td>yyyyMMddhhmmss</td></tr>
<tr><td>id_db </td><td>unambiguous number of MV-Grid    </td><td>integer       </td></tr>
<tr><td>geom  </td><td>geometric coordinates            </td><td>WGS84 POINT   </td></tr>
<tr><td>name  </td><td>FIXME                            </td><td>string        </td></tr>
<tr><td>status</td><td>FIXME                            </td><td>string        </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mvlv_mapping.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name        </th><th>description                                             </th><th>unit   </th></tr>
</thead>
<tbody>
<tr><td>id          </td><td>unambiguous unique numer                                </td><td>integer</td></tr>
<tr><td>run_id      </td><td>time and date of table generation in yyyyMMddhhmmss     </td><td>integer</td></tr>
<tr><td>lv_grid_id  </td><td>unambiguous number of LV-Grid                           </td><td>integer</td></tr>
<tr><td>lv_grid_name</td><td>unambiguous name: 'LVGridDing0_LV_#lvgridid#_#lvgridid#'</td><td>string </td></tr>
<tr><td>mv_grid_id  </td><td>unambiguous number of MV-Grid                           </td><td>integer</td></tr>
<tr><td>mv_grid_name</td><td>unambiguous name: 'MVGridDing0_MV_#mvgridid#_#mvgridid#'</td><td>string </td></tr>
</tbody>
</table>
@snapend

---
@snap[north span-80]
### mv_load.json
@snapend

@snap[midpoint span-100 text-04]
<table>
<thead>
<tr><th>name         </th><th>description                                                                               </th><th>unit          </th></tr>
</thead>
<tbody>
<tr><td>id           </td><td>unambiguous unique numer                                                                  </td><td>integer       </td></tr>
<tr><td>run_id       </td><td>time and date of table generation                                                         </td><td>yyyyMMddhhmmss</td></tr>
<tr><td>name         </td><td>unambiguous name: 'MVLoadDing0_MV_#mvgridid#_#ascendingnumber#'                           </td><td>string        </td></tr>
<tr><td>geom         </td><td>geometric coordinates                                                                     </td><td>WGS84 GEOMETRY</td></tr>
<tr><td>is_aggregated</td><td>True if load is aggregated load, else False                                               </td><td>boolean       </td></tr>
<tr><td>consumption  </td><td>type of load {retail, residential, agricultural, industrial} and corresponding consumption</td><td>string        </td></tr>
</tbody>
</table>
@snapend

