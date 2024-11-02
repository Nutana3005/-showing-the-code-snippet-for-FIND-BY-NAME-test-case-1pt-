# -showing-the-code-snippet-for-FIND-BY-NAME-test-case-1pt-
def test_find_product_by_name(self):
    # Create a product with a unique name
    product = Product(name="UniqueProductName", category="Category1", available=True)
    product.save()
    
    # Retrieve the product by name
    found_product = Product.find_by_name("UniqueProductName")
    
    # Assert that the retrieved product matches the created product
    assert found_product is not None
    assert found_product.name == "UniqueProductName"
