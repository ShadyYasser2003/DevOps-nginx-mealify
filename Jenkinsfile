pipeline {
    agent any  
    
    stages{
            stage('Checkout SCM') { // مرحلة استخراج الكود من Git
                steps {
                    git branch: 'main', // تحديد الفرع الرئيسي
                        url: 'https://github.com/ShadyYasser2003/nginx-mealify.git'
                    }
                }
        }
}