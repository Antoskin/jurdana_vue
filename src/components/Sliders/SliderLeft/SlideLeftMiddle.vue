<template>
            <div class="left-slide-mid">
                    <p>LEGAL SERVICES</p>
                    <h3>Our services</h3>
                    <nav>
                        <a href="#" v-for="item in menu">{{ item.menu_item }}</a>
                    </nav>
                    <div class="send-btn-lef">
                        Contact Us
                    </div>
            </div>
</template>


<script>
    const nav_menu = [
        {menu_item: 'Real estate & construction'},
        {menu_item: 'Corporate & Antitrust'},
        {menu_item: 'Intellectual property'},
        {menu_item: 'White collar crime'},
        {menu_item: 'Taxation'},
        {menu_item: 'Dispute resolution'},
        {menu_item: 'Private clients'},
    ]

    export default {
        name: 'SlideLeftMiddle',
      
        data: () => {
            return {
                menu: nav_menu
            }
        }
    }
</script>



<style scope>
.left-slide-mid
{
	align-items: center;
	color: #fff;
	display: flex;
	flex-direction: column;
	height: 100%;
	justify-content: center;
	// opacity: 0;
	text-align: center;
	// visibility: hidden;
}
h3
{
	padding: 30px 0;
}
nav
{
	align-self: center;
	display: flex;
	flex-direction: column;
	justify-content: space-around;
	text-align: center;
}
a
{
	color: #fff;
	margin: 5px 0;
	opacity: .7;
	text-decoration: none;
	transition: .3s ease-in-out;
}
a:hover
{
	opacity: 1;
}
.send-btn-lef
{
	background: transparent;
	border: 1px solid #fff;
	color: #fff;
	cursor: pointer;
	font-size: 30px;
	margin-top: 30px;
	padding: 10px 25px;
	transition: .5s ease-in-out;
}
.send-btn-lef:hover
{
	background: rgba(255,255,255,0.2);
}
</style>