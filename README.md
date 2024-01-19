# Kotlin
// class Aquarium(var width:Int = 20, var length:Int = 100, var height:Int = 40){
//     init{
//         println("Starting initializing Aquarium...")
//     }
//     init{
//         println("Volume: ${width * height * length} liters")
//     }
    
//     constructor(numberOfFish:Int) : this(){
//         val tank = numberOfFish * 2000 * 1.1 
//         height = (tank / (width * length)).toInt()
//         println("Высота равна: $height")
//     }
//     fun printSize(){
//         println("Width: $width cm" + " Length: $length cm" + " Height: $height cm")
//     }
// }
// fun buildAquarium(){
//     val myAquarium1 = Aquarium(numberOfFish = 76)
//     myAquarium1.printSize()
    
// }
class Product(var number: Int, var name: String , var price: Int , var quantity: Int ){ 
      fun printInfo() {
        println("Number: $number, Name: $name, Price: $price руб, Quantity: $quantity шт.")
    }
}
  
 fun buildProduct(){
     val product = Product(1, "fish", 159, 3)
    product.printInfo()
 }

fun main() {
   //buildAquarium()
   buildProduct()
   val invoice = arrayOf(Product(number = 2,name = "bike", price = 299, quantity = 4),
                         Product(number = 3,name = "skate", price = 199, quantity = 2))
 
 var sum = 0
 for (product in invoice) {
     sum += product.price * product.quantity
        product.printInfo()
    }
 println(sum)

    // Вариант 2: Метод forEach
    //invoice.forEach { it.printInfo() }
 
} 
