class student{
            private $name;
            public function __get($property){
                echo "$property is not exists";
            }

            public function __set($property, $value){
                if(property_exists($this,$property)){
                    $this->$property = $value;
                }else{
                    echo "Property not exists: $property";
                }
            }
            public function hello(){
                echo $this->name;
            }
        }
        $test = new student();
        $test->name = "Yahoo babas";

        $test->hello();
