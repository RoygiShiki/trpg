<template>
	<div class="filecard">
		<el-container>
			<el-main>
				<el-row>
					<el-col :span="20" :offset="2">
						<div class="grid-content">
							<el-container>
								<el-main>
									<el-row>
										<el-col :span="8">
											<div class="grid-content">
												<el-upload class="avatar-uploader"
													action="https://jsonplaceholder.typicode.com/posts/"
													:show-file-list="true" :on-success="handleAvatarSuccess">
													<img class="avatar" v-if="imageUrl" :src="imageUrl">
													<i class="el-icon-plus avatar-uploader-icon"></i>
												</el-upload>
											</div>
										</el-col>

										<el-col :span="16">
											<el-main class="radius">
												<div class="grid-content">
													<el-input class="mb-20" placeholder="姓名"></el-input>
													<el-input class="mb-20" placeholder="玩家"></el-input>
													<el-select class="mb-20 wid-100" placeholder="時代">
														<el-option>1</el-option>
														<el-option>2</el-option>
														<el-option>3</el-option>
													</el-select>
													<el-input class="mb-20" placeholder="年龄"></el-input>
													<el-input class="mb-20" placeholder="性別"></el-input>
													<el-input class="mb-20" placeholder="住地"></el-input>
													<el-input class="mb-0" placeholder="故乡"></el-input>
												</div>
											</el-main>
										</el-col>
									</el-row>
								</el-main>
							</el-container>
						</div>
					</el-col>
				</el-row>
				
				<el-row>
					<el-col :span="20" :offset="2">
						<el-main>
							<div class="radius">
								<el-main>
									<div>
										<el-select class="mb-20 wid-100" placeholder="职业" v-model="occupation">
											<el-option v-for="item in items" :key="item.value" :label="item.label" :value="item.value"></el-option>
										</el-select>
									</div>
									
									<div class="mb-20">本职技能：会计，法律，图书馆，聆听，说服，侦查，任意其他两项个人或时代特长。</div>
									
									<el-row>
										<el-col :span="6">
											<div>信用评级范围：30~70</div>
										</el-col>
										
										<el-col :span="6">
											<div>本职技能点：教育×4</div>
										</el-col>
										
										<el-col :span="6">
											<div>兴趣技能点：智力×2</div>
										</el-col>
									</el-row>
								</el-main>
							</div>
						</el-main>
					</el-col>
				</el-row>
				
				<el-row>
					<el-col :span="20" :offset="2">
						<el-main>
							<div class="radius">
								<el-main>
									<el-row>
										<el-col :span="6" class="radius">
											<el-main>
												<div class="sub-title">力量 STR</div>
												<el-input size="mini" class="mb-20" placeholder="力量 STR"></el-input>												
												
												<div class="sub-title">体质 CON</div>
												<el-input size="mini" class="mb-20" placeholder="体质 CON"></el-input>												
												
												<div class="sub-title">体型 SIZ</div>
												<el-input size="mini" class="mb-20" placeholder="体型 SIZ"></el-input>												
												
												<div class="sub-title">敏捷 DEX</div>
												<el-input size="mini" class="mb-20" placeholder="敏捷 DEX"></el-input>												
												
												<div class="sub-title">外貌 APP</div>
												<el-input size="mini" class="mb-20" placeholder="外貌 APP"></el-input>												
												
												<div class="sub-title">智力 INT</div>
												<el-input size="mini" class="mb-20" placeholder="智力 INT"></el-input>												
												
												<div class="sub-title">意志 POW</div>
												<el-input size="mini" class="mb-20" placeholder="意志 POW"></el-input>												
												
												<div class="sub-title">教育 EDU</div>
												<el-input size="mini" class="mb-20" placeholder="教育 EDU"></el-input>												
												
												<div class="sub-title">幸运 LUCK</div>
												<el-input size="mini" class="mb-20" placeholder="幸运 LUCK"></el-input>		
																						
												<div class="mb-20">总值(除幸运)：</div>
												<div><el-button type="primary" size="mini">随机属性</el-button></div>
											</el-main>
										</el-col>
										
										<el-col :span="6" :offset="2" class="radius">
											<el-main>
												<div class="sub-title">体力</div>
												<el-input size="mini" class="mb-20" placeholder="体力"></el-input>												
												
												<div class="sub-title">魔力</div>
												<el-input size="mini" class="mb-20" placeholder="魔力"></el-input>												
												
												<div class="sub-title">移动</div>
												<el-input size="mini" class="mb-20" placeholder="移动"></el-input>												
												
												<div class="sub-title">理智</div>
												<el-input size="mini" class="mb-20" placeholder="理智"></el-input>												
												
												<div class="sub-title">体格</div>
												<el-input size="mini" class="mb-20" placeholder="体格"></el-input>
												
												<div class="radius-buttom mb-20"></div>
												
												<div class="sub-title">伤害加值</div>
												<el-input size="mini" class="mb-20" placeholder="伤害加值"></el-input>
												
												<div class="sub-title">身体状态</div>
												<el-select class="mb-20 wid-100" placeholder="身体状态" size="mini">
													<el-option>健康</el-option>
												</el-select>
												
												<div class="sub-title">精神状态</div>
												<el-input size="mini" class="mb-20" placeholder="精神状态"></el-input>
											</el-main>
										</el-col>
									</el-row>
								</el-main>
							</div>
						</el-main>
					</el-col>
				</el-row>
			</el-main>
		</el-container>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				name: 'rpg',
				imageUrl: '',
				occupation: 'counter',
				items: [{
					value: 'counter',
					label: '会计师'
				},{
					value: 'actor',
					label: '演员'
				}]
			}
		},

		methods: {
			handleAvatarSuccess(res, file) {
				this.imageUrl = URL.createObjectURL(file.raw);
			},
		}
	}
</script>

<style lang="scss">
	.avatar-uploader {
		.el-upload {
			border: 1px dashed #d9d9d9;
			border-radius: 6px;
			cursor: pointer;
			position: relative;
			overflow: hidden;
		}

		.el-upload:hover {
			border-color: #409EFF;
		}

		.avatar-uploader .el-upload:hover {
			border-color: #409EFF;
		}

		.avatar-uploader-icon {
			font-size: 28px;
			color: #8c939d;
			width: 220px;
			height: 220px;
			line-height: 220px;
			text-align: center;
		}

		.avatar {
			width: 178px;
			height: 178px;
			display: block;
		}
	}
	
	.wid-100 {
		width: 100%;
	}
	
	.radius-buttom {
		border-bottom: 1px solid #d7dae2;
	}
</style>
