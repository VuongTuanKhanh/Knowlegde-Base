# Search App Conversation

## Resource
---
|Content|Link|
|:--|:--|
|**Chatport**|https://app.chaport.com/#/chats/3e61882c-97b4-48df-9f2e-0d402082174f/1598545489432 <br> **Username**: `support@sobooster.com` <br> **Password**: `Nga@1234`|
|**Q&A**|https://docs.google.com/document/d/1IJCyCq8dPS0cbBxICpBGcvxOkpNQIlfMg2V5Os-oDes/edit?ts=5f47e9e4|
|**Supported Theme List**|https://docs.sobooster.com/search/integration/ultimate-filter-search-shopify-theme-integration|
|**Shopify Admin**|https://khanhvuongstore.myshopify.com/admin|
|**Developer Document**|https://docs.sobooster.com/search/developer/usf-sdk|
|**USF App**|https://app.usf.test/khanhvuongstore-myshopify-com#/collections/pins|
|**Requirement App**|https://airtable.com/|

 
## Q&A Translation
---
### 1. Why filter not show up ?
- Vào phần `Filter` trong mục `Settings`.
- Kiểm tra xem theme đang sử dụng `Filter Group` tự tạo hay `Default Filter Group`.
- Kiểm tra các `Filter` con nằm trong từng `Filter Group`:
    - Nếu `Filter Group` đó rỗng, phải thêm các `Filter` con vào bên trong vì nếu không có điều kiện thì `Filter` không có gì để lọc. Ở trường hợp này, người dùng thường nhầm lẫn rằng khi đã tạo `Filter Group` là xong, không cần làm gì thêm, dẫn đến việc thiếu điều kiện.
    - Kiểm tra từng `Filter` con, trường hợp hay xảy ra nhất đó là thiếu `Tag Prefix` trong tên product. Người dùng hay nhầm lẫn `Label` và `Tag Prefix`.
- Vào phần `Filter` trong mục `Settings` và enable `Turn on Show filter options`.
- Kiểm tra theme đã được hỗ trợ chưa:
    - Mở console và nhập `Shopify.theme`, lấy `id`.
    - Paste `id` vừa nhận vào link: `storename.myshopify.com/?preview_theme_id=...`
    - Mở console và nhập `_usfTheme`:
        - 1 = Theme supported.
        - 0 = Theme not supported.
- **Thời hạn xử lý:** *Our development team will check the theme support and get back to you asap.” I would expect it to be done in 1-2 business days.*

### 2. Why collection do not show anything (or no results found)?
- Mở `Settings`, truy cập mục `Status & Usage`.
- Enable các mục:
    - `All Ultimate Search solution`.
    - `Search page`.
    - `Collection page`.

### 3. Set filter values order, i.e. Size “S, M, L” or :2,4,6,8,10,12” ?
- https://docs.sobooster.com/search/product-filtering-guide/set-manual-values

### 4. Set filter values order, i.e. Size “S, M, L” or :2,4,6,8,10,12”  but not showing correctly?
- Giống trường hợp trên, tuy nhiên nhắc người dùng phải bỏ chọn `Sort manual values`.

### 5. How to filter by metafield?
- https://docs.sobooster.com/search/product-filtering-guide/filter-collections-using-metafields
- Check product data. Ask for product URL (product that has metafields) → Search by product title > Press F12 > Check Network/ XHR > Find source from search > Click on items (right column) > Metafield > Check matatield (namespace.key).
If merchants add wrong namespace.key to Settings/ Search index in app > Correct the metafield in Search index > Click Sync > Go to Filters > Add metafields to the filter group.

### 6. How to hide vendor? 
- Vào phần `Settings/ Advanced/ Search results settings`, chọn `Disable show vendor`.
- Sau đó, kiểm tra bằng cách search trên thanh searchbar, nếu vẫn hiện vendor, phải ẩn bằng CSS. Kiểm tra tương tự ở phần Collection ( cả Gridview và Listview ).

### 7. How to remove Add to cart and Quick view rendered by app?
- Tắt Plugin ở mục `Plugin`.
- Some themes (Warehouse, …) render Quich view and Add to cart from theme settings → Turn off Quick buy and Choose option in Themes/ Customization/ Collection/ Theme settings (Only on Collection). On Search results page (rendered by USF) → Hide Quick view and Add to cart by CSS (Check element).

### 8. Why merchandising rule in Collection does not working?
- Ask merchants to check if the collection is Shopify admin is set Sort by manual. If it’s set up “Sort by Manual” in Shopify admin, it will override the Merchandising rule/ Pinning in app. → Ask merchants to change the sort field (any field except for Manual).
- Check default sorting (the top) in app Settings/ Advanced is set to Best selling. If it’s set up default sorting by Best selling, it will override the Merchandising rule/ Pinning in app. → Ask merchants to change the default sort field (any field except for Best selling).

### 9. How to hide filter on specific collection/ search results page?
- Tạo thêm `Filter Group` rỗng cho các `Collection` đó.

### 10. How to re-order/ arrange the filter option (for example, Brand, Product type, Price, Color, Size) ?
- Vào phần "Filter", chọn "Filter Group" cần chỉnh sửa.
- Kéo thả thứ tự các `Filter` con.

### 11. How to merge filter values ?
- Vào `Settings`, chọn `Merged values`, ấn nút `Merge values`

### 12. Filter by Size/ Color (after merging) are missing the products in the list ?
- Kiểm tra điều kiện của `Merge Value` có rỗng không, nếu không rỗng thì thử kiểm tra trước khi merge thì các `Filter` con có giá trị trước khi merge không. ( Cột trái của `Settings / Merge vale ).

### 13. Set up Filter by Collection and Sub-category? (Main category and Sub category) ?
- https://docs.sobooster.com/search/product-filtering-guide/navigation-collections
    - Chọn vào `Filter Group` cần sửa.
    - Thêm `Filter` con.
    - Chọn `Option` là `Collection`.
    - Gán `Label`
    - Chọn ` Navigation Collection`.
    - Chọn các `Subcategory`.

### 14. Product grid does not look the same like theme before installing app ?
- Kiểm tra theme gốc như ở phần 1, preview theme gốc.
- Preview theme sau khi cài app và so sánh.
- Check theme after installing app (in Customization > See theme name set up with app - Get theme ID by selecting theme and copy URL or check by theme ID in theme script tool)
- Open one theme in Incognito mode (Ctrl + Shift + N) → Compare 2 layouts. If there any third party app that USF does not integrate → “Our development team will check the integration with……………and get back to you asap.” I would expect it to be done in 1-2 business days. (If merchants ask how much time/ how long).

### 15. Show percent discount label? My theme shows discount percent (-20%) label, after installing the app, it shows Sale label. How to change it back to percent discount label ?
- Vào `Customization/ Select theme / Javascript`.
- Thêm function: `usfSalePercent = function (p)`.
- Thay tất cả `loc.sale` bằng `usfSalePercent(product)`.

### 16. Show variants as separate products? Is this feature available during trial ?
- Vào `Settings/ Premium feature`, enable `Show variants as separate products`, sau đó chọn các option.
- Add option to the product title in Instant Search, Collection and Search results page. For example, product title, color A; product title, color B. Edit in customization/ Select theme / Javascript. See sample JS codes.

### 17. I want to change numbers of products per row (3 products per row, 4 product per row)?
- Đăng nhập https://search-app.sobooster.com/ 
- Vào phần `Check in Customization`
    - Nếu có nhiều hơn một theme, kiểm tra xem live theme có đang cài app không
    - Nếu có, vào console, nhập `Shopify.theme` để lấy tên theme, sau đó chỉnh sửa code của theme đó.
