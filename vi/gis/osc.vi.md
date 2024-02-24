{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Thay đổi định dạng tệp",
  "description":"Tìm hiểu về định dạng tệp OSC và các API có thể tạo và mở tệp OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-vi",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Tập tin OSC là gì?

Tệp OSC là Định dạng tệp thay đổi chứa dữ liệu bản đồ đường phố đã sửa đổi cho bản đồ đường phố .osm hiện có. Nó chứa thông tin về những thay đổi sẽ xảy ra đối với [OSM file](/gis/osm/). Tệp OSC có thể có ba loại hoạt động sửa đổi có thể có trên dữ liệu OSM, tức là `chèn`, `sửa đổi` hoặc `xóa`. Các tệp thay đổi này thường được sử dụng để xuất dữ liệu ra khỏi trình soạn thảo OSM và nhập vào trình chỉnh sửa khác.

Bạn có thể mở tệp OSC bằng phần mềm Merkaartar và osmchange.

## Định dạng tệp OSC

Các tệp OSC thường được lưu ở định dạng tệp JOSM trong đó các thay đổi được biểu thị bằng thẻ. Nó bắt đầu bằng thẻ `osmChange` cho biết phần đầu của tệp. Các thẻ phụ chỉ định xem đó là thao tác chèn, sửa đổi hoặc xóa sẽ được thực hiện trên nút tương ứng trong tệp OSM. Nội dung của một nút thực sự chứa nội dung của thẻ osm.

### Ví dụ về định dạng tệp OSC

Sau đây là một ví dụ về thao tác sửa đổi trên một nút. Mỗi phần tử phải có ID bộ thay đổi và số phiên bản.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Người giới thiệu

* [Định dạng tệp JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


