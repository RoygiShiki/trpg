<template>
	<div class="about">
		<el-container>
			<el-header>属性</el-header>
			<el-main>
				<el-row>
					<el-col :span="8" :offset="8">
						<div class="grid-content">
							<el-input placeholder="力量"></el-input>
						</div>
					</el-col>
				</el-row>
				
				<el-row>
					<el-col :span="8" :offset="8">
						<div class="grid-content">
							<el-input placeholder="敏捷"></el-input>
						</div>
					</el-col>
				</el-row>
				
				<el-row>
					<el-col :span="8" :offset="8">
						<div class="grid-content">
							<el-input placeholder="智力"></el-input>
						</div>
					</el-col>
				</el-row>
				
				<el-row>
					<el-col :span="8" :offset="8">
						<div class="grid-content">
							<el-input placeholder="幸运"></el-input>
						</div>
					</el-col>
				</el-row>
				
				<el-row>
					<el-col :span="8" :offset="8">
						<div class="grid-content">
							<el-input placeholder="速度"></el-input>
						</div>
					</el-col>
				</el-row>
				
				<el-button type="primary">提交<i class="el-icon-upload el-icon--right"></i></el-button>
			</el-main>
			<!-- <el-footer>到底啦</el-footer> -->
		</el-container>
	</div>
</template>
