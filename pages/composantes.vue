<template>
    <div>
        <NavOne />
        <PageHeader title="Composantes du PFC BENIN" />
        <!-- <CourseOne /> -->

        <CourseCategory />
        <Footer />
    </div>
</template>
<script>
import CourseCategory from "../components/CourseCategory";
import PageHeader from "../components/PageHeader";
import NavOne from "../components/NavOne";
import Footer from "../components/Footer";
export default {
    components: { Footer, NavOne, PageHeader, CourseCategory },
    head() {
        return {
            title: "PFC BENIN | Composantes du PFC BENIN"
        }
    }
}
</script>