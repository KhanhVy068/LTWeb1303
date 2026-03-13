Báo cáo lập trình web nhóm 13 
Các lỗi tìm được
+**File: orders.php**    
- Lỗi 1: Logic
Trước khi sửa:
foreach ($orders as $order) {
    if ($order['status'] === 'completed') {
        $pendingOnly[] = $order;
    }
}
Sau khi sửa: 
foreach ($orders as $order) {
    if ($order['status'] === 'pending') {
        $pendingOnly[] = $order;
    }
}
**File: checkout.php**
- Lỗi 2: Logic
Trước khi sửa:
foreach ($cart as $item) {
    $subtotal = $products[$item['sku']]['price'] * $item['qty'];
}
Sau khi sửa:
foreach ($cart as $item) {
    $subtotal += $products[$item['sku']]['price'] * $item['qty'];
}
**dashboard.php**
- Lỗi 3: Logic
Trước khi sửa:
if ($order['status'] === 'pending') {
    $completedOrders++;
    $totalRevenue += calculate_order_total($order, $products);
}
Sau khi sửa:
if ($order['status'] === 'completed') {
    $completedOrders++;
    $totalRevenue += calculate_order_total($order, $products);
}

- Lỗi 4: Logic
Trước khi sửa:
if ($product['stock'] < 1) {
Sau khi sửa:
if ($product['stock'] < 5) {

**customer.php**
- Lỗi 5: syntax
Trước khi sửa:
if ($customer['active') { 
Sau khi sửa: 
if ($customer['active']) { 
**report.php**
- Lỗi 6: syntax
Trước khi sửa:
$reportRows = []
Sau khi sửa:
$reportRows = [];
**setting.php**
- Lỗi 7: syntax
Trước khi sửa: 
$config = [
    'currency' => 'USD',
    'timezone' => 'Asia/Ho_Chi_Minh',
    'language' => 'en',
;
Sau khi sửa:
$config = [
    'currency' => 'USD',
    'timezone' => 'Asia/Ho_Chi_Minh',
    'language' => 'en',
];

